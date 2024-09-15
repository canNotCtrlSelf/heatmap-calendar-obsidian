```dataviewjs
dv.span("**🔗 Writing **- Don't break the chain! 🔗🔗🔗🔗")

const calendarData = {
    //year: 2022, // optional, remove this line to autoswitch year
    colors: {
        white: ["#F9F1AD"],
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
        font-size: 15px; /* Adjust the size as needed */
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 100%;
    }
`;
document.head.appendChild(style);

```