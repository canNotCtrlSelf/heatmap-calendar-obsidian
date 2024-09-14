---
date: 2024-09-14
source:
  - https://www.color-hex.com/
---

```dataviewjs
dv.span("**💪 Exercise 💪**")

const calendarData = {
    //year: 2022, // optional, remove this line to autoswitch year
    colors: {
        red: ["#ff9e82","#ff7b55","#ff4d1a","#e73400","#bd2a00",]
    },
    entries: []
}

for(let page of dv.pages('"300_Other/Daily Notes"').where(p=>p.exercise)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.exercise,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)

```

---

```dataviewjs
dv.span("**😊 Mood 😊**")

const calendarData = {
    //year: 2024, // optional, remove this line to autoswitch year
    colors: {
        //white: ["#F9F1AD"],
        transparent: ["transparent"],
    },
    entries: []
}

// Define mood icons
const moodIcons = {
    1: '😞', // Very sad
    2: '😟', // Sad
    3: '😕', // Disappointed
    4: '😐', // Neutral
    5: '🙂', // Slightly happy
    6: '😊', // Happy
    7: '😀', // Very happy
    8: '😃', // Excited
    9: '😄', // Ecstatic
    10: '😆' // Overjoyed
}

for(let page of dv.pages('"300_Other/Daily Notes"').where(p => p.mood)){
    const mood = page.mood;
    const icon = moodIcons[mood] || '😐'; // Default to neutral if mood is not in the range
    calendarData.entries.push({
        date: page.file.name,
        content: await dv.span(`<span class="heatmap-icon">${icon}</span>`), // for hover preview
    })
}

//console.log(calendarData)
renderHeatmapCalendar(this.container, calendarData)

// Add custom CSS to style the icons
const style = document.createElement('style');
style.innerHTML = `
    .heatmap-icon {
        font-size: 18px; /* Adjust the size as needed */
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 100%;
    }
`;
document.head.appendChild(style);

```

---

```dataviewjs
dv.span("**💤 Slepp 💤**")

const calendarData = {
    //year: 2022, // optional, remove this line to autoswitch year
    colors: {
        red: ["#ffffff","#ffffff","#ffffff","#ece5ee","#d9ccdd","#c6b3cc","#b39abb","#a081aa","#8d6799","#7a4e88","#663576","#541c66","#410355"]
    },
    defaultEntryIntensity: 7,   // (optional) defaults to 4
	intensityScaleStart: 0,    // (optional) defaults to lowest value passed to entries.intensity
	intensityScaleEnd: 13,     // (optional) defaults to highest value passed to entries.intensity
    entries: []
}

for(let page of dv.pages('"300_Other/Daily Notes"').where(p=>p.sleep)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.sleep,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)

```

---

```dataviewjs
dv.span("**🔠 English Reading 🔠**")

const calendarData = {
    //year: 2022, // optional, remove this line to autoswitch year
    colors: {
        blue: ["#99acf4","#859bf2","#708af0","#5c7aee","#4869ec","#3459ea"]
    },
    defaultEntryIntensity: 1,   // (optional) defaults to 4
	intensityScaleStart: 0,    // (optional) defaults to lowest value passed to entries.intensity
	intensityScaleEnd: 6,
    entries: []
}

for(let page of dv.pages('"300_Other/Daily Notes"').where(p=>p.english_reading)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.english_reading,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)

```

---

```dataviewjs
dv.span("**📖 Daily Reading 📖**")

const calendarData = {
    //year: 2022, // optional, remove this line to autoswitch year
    colors: {
        green: ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
    },
    defaultEntryIntensity: 1,   // (optional) defaults to 4
	intensityScaleStart: 0,    // (optional) defaults to lowest value passed to entries.intensity
	intensityScaleEnd: 6,
    entries: []
}

for(let page of dv.pages('"300_Other/Daily Notes"').where(p=>p.daily_reading)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.daily_reading,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)

```

---

```dataviewjs
dv.span("**🐧 Linux Learning 🐧**")

const calendarData = {
    //year: 2022, // optional, remove this line to autoswitch year
    colors: {
        green: ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
    },
    defaultEntryIntensity: 1,   // (optional) defaults to 4
	intensityScaleStart: 0,    // (optional) defaults to lowest value passed to entries.intensity
	intensityScaleEnd: 6,
    entries: []
}

for(let page of dv.pages('"300_Other/Daily Notes"').where(p=>p.linux_learning)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.linux_learning,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)

```

---

```dataviewjs
dv.span("**📝 UP Project 📝**")

const calendarData = {
    //year: 2022, // optional, remove this line to autoswitch year
    colors: {
        orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"]
    },
    defaultEntryIntensity: 1,   // (optional) defaults to 4
	intensityScaleStart: 0,    // (optional) defaults to lowest value passed to entries.intensity
	intensityScaleEnd: 6,
    entries: []
}

for(let page of dv.pages('"300_Other/Daily Notes"').where(p=>p.up_project)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.up_project,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)

```

---

```dataviewjs
dv.span("**🎮 Play Games 🎮**")

const calendarData = {
    //year: 2022, // optional, remove this line to autoswitch year
    colors: {
        pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
    },
    defaultEntryIntensity: 1,   // (optional) defaults to 4
	intensityScaleStart: 0,    // (optional) defaults to lowest value passed to entries.intensity
	intensityScaleEnd: 6,
    entries: []
}

for(let page of dv.pages('"300_Other/Daily Notes"').where(p=>p.play_games)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.play_games,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)

```

---

```dataviewjs
dv.span("**🎞️ Watch Movie 🎞️**")

const calendarData = {
    //year: 2022, // optional, remove this line to autoswitch year
    colors: {
        orange: ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
    },
    defaultEntryIntensity: 1,   // (optional) defaults to 4
	intensityScaleStart: 0,    // (optional) defaults to lowest value passed to entries.intensity
	intensityScaleEnd: 6,
    entries: []
}

for(let page of dv.pages('"300_Other/Daily Notes"').where(p=>p.watch_movie)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.watch_movie,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)

```

---

```dataviewjs
dv.span("**🎵 Listen Music 🎵**")

const calendarData = {
    //year: 2022, // optional, remove this line to autoswitch year
    colors: {
        green: ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
    },
    defaultEntryIntensity: 1,   // (optional) defaults to 4
	intensityScaleStart: 0,    // (optional) defaults to lowest value passed to entries.intensity
	intensityScaleEnd: 6,
    entries: []
}

for(let page of dv.pages('"300_Other/Daily Notes"').where(p=>p.listen_music)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.listen_music,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)

```

