---
title: "File Extension Analyzer"
description: "Returns the possible file extension of a file"
draft: false
---

<script defer>
async function onSubmit(event) {
    event.preventDefault();
    let file = document.getElementById('file');
    let result = document.getElementById('result');
    let tbody = document.getElementById('tbody');
    let msg = document.getElementById('msg');

    if (file.files.length === 0) {
        msg.innerHTML = "Please select a file.";
        return;
    }

    let data = new FormData();
    data.append('file', file.files[0]);

    let dataReturned = await fetch('http://trid.tools.ilikechicken.me/upload', {
        method: 'POST',
        body: data
    })

    if (dataReturned.status !== 200) {
        msg.innerHTML = "Error: " + dataReturned.status;
        return;
    }

    let dataJson = await dataReturned.json();


    msg.innerHTML = "";
    tbody.innerHTML = "";

    if (dataJson.msg && dataJson.msg === "File is in plain text") {
        msg.innerHTML = "File is in plain text";
        return;
    }

    for (let i = 0; i < dataJson.probabilities.length; i++) {
        let tr = document.createElement('tr');
        let td1 = document.createElement('td');
        let td2 = document.createElement('td');
        let td3 = document.createElement('td');
        td1.innerHTML = i+1;
        td2.innerHTML = dataJson.probabilities[i].name;
        td3.innerHTML = dataJson.probabilities[i].probability;
        tr.appendChild(td1);
        tr.appendChild(td2);
        tr.appendChild(td3);
        tbody.appendChild(tr);
    }
}

</script>
<input onchange="onSubmit(event)" type="file" id="file" name="file" class="form-control" style="display: inline">
<h2 id="msg" style="margin-top: 10px"></h2>
<div id="result">
    <table class="table file-table">
        <thead>
            <tr>
                <th scope="col">#</th>
                <th scope="col">File Extension</th>
                <th scope="col">Probability</th>
            </tr>
        </thead>
        <tbody id="tbody">
        </tbody>
    </table>
</div>