// Selecting elements from the DOM
const buttonName = document.getElementById('changeName');
const studentName = document.getElementById('studentName');

const buttonBg = document.getElementById('changeBackground');
const profileContainer = document.querySelector('.profile-container');

const buttonToggle = document.getElementById('toggleDetails');
const studentDetails = document.getElementById('studentDetails');

// 1. Change Name Button functionality
buttonName.addEventListener("click", function() {
    studentName.textContent = "Maria Santos";
});

// 2. Change Background Button functionality
buttonBg.addEventListener("click", function() {
    if (profileContainer.style.backgroundColor === "rgb(240, 253, 250)") {
        profileContainer.style.backgroundColor = "white";
    } else {
        profileContainer.style.backgroundColor = "#f0fdfa";
    }
});

// 3. Show/Hide Details Button functionality
buttonToggle.addEventListener("click", function() {
    studentDetails.classList.toggle('hidden');
    
    // Toggle button label text accordingly
    if (studentDetails.classList.contains('hidden')) {
        buttonToggle.textContent = "Show/Hide Details";
    } else {
        buttonToggle.textContent = "Hide Details";
    }
});
