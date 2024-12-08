const channels = [
    {
        name: "Канал 1",
        logo: "https://via.placeholder.com/150",
        programs: ["Передача 1", "Передача 2", "Передача 3"]
    },
    {
        name: "Канал 2",
        logo: "https://via.placeholder.com/150",
        programs: ["Передача 4", "Передача 5"]
    },
    {
        name: "Канал 3",
        logo: "https://via.placeholder.com/150",
        programs: ["Передача 6", "Передача 7", "Передача 8"]
    }
];

function displayChannels() {
    const channelList = document.getElementById('channel-list');
    channels.forEach(channel => {
        const card = document.createElement('div');
        card.className = 'channel-card';
        card.innerHTML = `
            <img src="${channel.logo}" alt="${channel.name}">
            <h2>${channel.name}</h2>
            <p>Программы:</p>
            <ul>
                ${channel.programs.map(program => `<li>${program}</li>`).join('')}
            </ul>
        `;
        channelList.appendChild(card);
    });
}

document.addEventListener('DOMContentLoaded', displayChannels);
