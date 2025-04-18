<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>Caribbean Coast Shuttle — Next Buses</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
  body{font-family:-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
       display:flex;flex-direction:column;align-items:center;justify-content:center;min-height:100vh;margin:0}
  h1{margin:0.2em;font-size:2rem}
  #clock{font-size:1.25rem;margin-bottom:1em}
  ul{list-style:none;padding:0;font-size:2.5rem;margin:0}
  li{margin:0.1em 0}
</style>
<script src="data.js"></script>
</head>
<body>
  <h1 id="title"></h1>
  <div id="clock"></div>
  <ul id="list"></ul>

<script>
/* --- helper functions ---------------------------------------- */
function hhmmToDate(hhmm, baseDate){
  let h = parseInt(hhmm.slice(0,2),10),
      m = parseInt(hhmm.slice(2),10);
  let d = new Date(baseDate);
  d.setHours(h); d.setMinutes(m); d.setSeconds(0); d.setMilliseconds(0);
  // Times past midnight (0000‑0200) belong to "tomorrow" logically
  if(h < 3 && baseDate.getHours() >= 21) d.setDate(d.getDate()+1);
  return d;
}
function nextThree(now, list){
  return list
    .map(t => ({t, when: hhmmToDate(t, now)}))
    .filter(o => o.when >= now)
    .slice(0,3);
}
/* --- main ----------------------------------------------------- */
function refresh(){
  const params = new URLSearchParams(location.search),
        station = params.get("station") || "1",
        today   = new Date(),
        dow     = today.getDay(),            // 0=Sun … 6=Sat
        mode    = (dow===0 || dow===6) ? "weekend" : "weekday",
        list    = timetable[station][mode];
  // update page title
  document.getElementById("title").textContent =
     `Station ${station} — ${mode === "weekday" ? "Mon–Fri" : "Sat/Sun/Holidays"}`;

  // clock
  document.getElementById("clock").textContent =
     today.toLocaleTimeString([], {hour: "2-digit", minute:"2-digit", second:"2-digit"});

  // next three
  const next = nextThree(today, list);
  const ul = document.getElementById("list");
  ul.innerHTML = "";
  next.forEach(o=>{
      const li = document.createElement("li");
      li.textContent = o.t.slice(0,2)+":"+o.t.slice(2);
      ul.appendChild(li);
  });
}
refresh();
setInterval(refresh, 1000*30);       // update every 30 s
</script>
</body>
</html>
