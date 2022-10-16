---
title: "Timezone Converter"
description: "A timezone converter"
draft: false
---

<script src="/js/chrono.js" defer></script>
<script defer>
let typingTimer;
let doneTypingInterval = 2000;
let input = document.getElementById('time');
let show = document.getElementById('show-time');
let data;
input.addEventListener('keyup', function () {
    clearTimeout(typingTimer);
    if (input.value) {
        typingTimer = setTimeout(doneTyping, doneTypingInterval);      
    }
});
function doneTyping () {
    data = chrono.parseDate(input.value);
    if(data) {
        show.innerHTML = 'Converts to ' + data.toString();
    } else {
        show.innerHTML = "Unable to process the time."
    }
}
</script>
<input type="text" class="time" id="time" placeholder="Try 'next friday at 2 pm est'">
<h4 id="show-time"></h4>