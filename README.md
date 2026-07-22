# Route-Assignment-9
Project: Contact Hub - Smart Contact Manager
A feature-rich, dynamic contact management web application built with vanilla JavaScript, Bootstrap 5, and HTML5/CSS3. This project demonstrates state management, local storage persistence, dynamic UI rendering, real-time input validations, debounced search, and custom alert handling.

🚀 Project Overview
The application is structured into four main operational areas, providing a seamless contact management experience:

Contact Operations & Persistence: Complete CRUD functionality supported by browser LocalStorage to retain contact records across sessions.

Featured Contacts & Real-Time Counters: Dedicated sidebars for starred (Favorites) and emergency contacts, alongside dynamic counter widgets.

Real-time Validation & Duplicate Prevention: Multi-tier field validation using Regular Expressions and duplicate phone number checks.

Debounced Search & UI Interactions: Smooth user experience with debounced search filtering across multiple criteria and customizable visual avatars.

🛠 Technical Implementation
1. Contact Management & Persistence
LocalStorage Integration: Uses getLocalContacts() to fetch and parse JSON data from localStorage, maintaining full persistence across browser refreshes.

Dynamic Avatars: Implements createavatar() to automatically generate two-letter initials from full names and assigns a persistent random background color via getRandomColor() and avatarColors.

Modal State Switching: Utilizes setToUpdate() and updateContact() to toggle modal action states between "Save" and "Update", keeping track of active edit targets using currentIndex.

2. Sidebars & Counter Calculations
Real-time Counter Sync: Employs ES6 Object Destructuring (var { totalContacts, favoriteContacts, emergencyContacts } = getCounters()) and updates DOM counters efficiently using textContent.

Featured Contacts Lists: Features displayFeaturedContacts() to filter, construct, and inject side lists for Favorites and Emergency contacts with custom badge indicators.

Quick Toggle Actions: Implements toggleFavorite() and toggleEmergency() to quickly mutate contact boolean flags and re-render all dependent UI sections immediately.

3. Input Validation & Verification
Reusable Validation Helper: Uses a centralized validateField() helper function paired with custom Regular Expressions (nameRegex, phoneRegex, emailRegex) for real-time input feedback (is-invalid CSS states and error messages).

Optional vs. Required Logic: Supports optional field checking (e.g., email validation passes when empty but validates pattern when filled).

Duplicate Protection: Scans existing records to block duplicate phone numbers on creation and safely excludes the current editing index (index !== currentIndex) during contact updates.

4. Interactive UI & Debounced Search
Debounced Search: Uses setTimeout and clearTimeout inside searchContacts() to delay search execution by 600ms, reducing unnecessary calculations while filtering contacts by name, phone, or email.

SweetAlert2 Integration: Integrated rich alert dialogues for deletion confirmations, validation error alerts, and timed auto-dismissing success toasts.

Form Clean-up: Implements clearForm() to reset input values, checkbox states, red border classes, and hidden error elements after every action.

💻 How to Use
Clone the repository:

Bash
git clone https://github.com/NohaOmar20/contact-hub.git
Open the index.html file in any modern web browser.

Add, edit, star, or search contacts—all data will automatically save to your browser's local storage.

🎓 About the Author
Noha Omar is a Quality-driven Front-End Developer and UX/UI designer certified by Google. A Computer Science Engineering graduate from the Egypt-Japan University of Science and Technology (E-JUST), specializing in responsive web applications and AI-powered research.

* **LinkedIn:** [nohaomar](https://www.linkedin.com/in/nohaomar/)
* **GitHub:** [NohaOmar20](https://github.com/NohaOmar20)
* **Instagram:** [noha.omar._](https://www.instagram.com/noha.omar._/)

This project was created as a part of a Front-End development task to demonstrate state management, DOM manipulation, and dynamic user interface features using modern JavaScript.
