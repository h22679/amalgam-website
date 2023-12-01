---
# the default layout is 'page'
icon: fas fa-info-circle
order: 2
---

<div style="text-align:center;">
    Players online: <span id="player-count">Loading...</span>
</div>

---

<iframe style="width:100%; height:500px;" src="https://uptime.cocobut.net/status/mod-server"></iframe>

---

<iframe style="width:100%; height:700px;" src="https://map.cocobut.net/"></iframe>

<!--- > Add Markdown syntax content to file `_tabs/about.md`{: .filepath } and it will show up on this page.
{: .prompt-tip } --->

<script>
fetch('https://api.mcsrvstat.us/2/mods.cocobut.net')
    .then(response => response.json())
    .then(data => {
        if (data.online) {
            document.getElementById('player-count').textContent = data.players.online;
        } else {
            document.getElementById('player-count').textContent = 'Server Offline';
        }
    })
    .catch(error => {
        console.error('Error fetching player count:', error);
        document.getElementById('player-count').textContent = 'Error';
    });
</script>