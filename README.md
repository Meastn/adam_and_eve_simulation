# adam_and_eve_simulation
Open-source HTML5 game simulating human tribes’ survival, reproduction, and migration in a dynamic world. Inspired by Game of Life, built with Grok 3. Beta v0.5. See README for details. Players manage resources, seasons, and battles to grow humanity.
Adam and Eve: The Beginning
Open-source HTML5 game simulating human tribes’ survival, reproduction, and migration in a dynamic world. Inspired by Game of Life, built with Grok 3. Beta version 0.5. See below for details.
Version
Version 0.5 (Beta): This is an early beta release of "Adam and Eve: The Beginning." The game is functional but may contain bugs or incomplete features. We actively seek community feedback to refine and improve it before a stable release. Please report issues or suggest enhancements via GitHub Issues.
Overview
"Adam and Eve: The Beginning" is an open-source, browser-based survival simulation game that models the evolution of human tribes (descendants of Adam and Eve) in a procedurally generated, dynamic world. Drawing inspiration from Conway’s Game of Life, this project explores whether real human behaviors—such as reproduction, migration, resource management, and conflict—can be simulated effectively. The game was initially prototyped as a fun side project using ChatGPT 4, but with the power of Grok 3 by xAI, I was able to rewrite and enhance the entire codebase in a single day, adding all features without manually coding myself. My development process involved conceptualizing functions, refining ideas, requesting code generation from Grok, testing, and iterating based on Grok’s responses.
Purpose and Gameplay
"Adam and Eve: The Beginning" is a survival simulation game where players observe and interact with virtual tribes of humans (Adam and Eve’s descendants) as they navigate a dynamic world filled with diverse terrains like grasslands, forests, mountains, deserts, oceans, tundra, and coastlines. The goal is to ensure the survival and growth of humanity while managing resources, reproduction, and environmental challenges.
Key Features and Functions
Here’s a detailed breakdown of the game’s mechanics and features:
1. Procedural World Generation
The game generates a random, grid-based world using noise algorithms (Perlin/Simplex noise-inspired) to create realistic landscapes.
Terrains include grasslands (#27ae60), forests (#16a085), water (#3498db), mountains (#7f8c8d), deserts (#f1c40f), coastlines (#e67e22), and tundra (#95a5a6).
Rivers and lakes are procedurally added to enhance environmental diversity.
2. Tribal Dynamics
Players begin with a player-controlled tribe and can observe AI-controlled tribes as they grow, split, or migrate.
Tribes are represented by colored markers on the map, with mood emojis (😊, 😐, 😟, 😢) indicating stress levels.
Tribes split when population exceeds a configurable threshold (default 50) and conditions like stress and resource abundance allow.
3. Reproduction and Population Growth
Tribes reproduce based on a configurable reproduction rate (default 0.3), with infant mortality (default 0.05) and maternal mortality (default 0.02).
Reproduction requires at least one fertile female (aged 16–40) and one male (aged 16+). If only one gender remains (e.g., 1 male, 0 females or vice versa), reproduction stops, and the tribe faces extinction upon the last individual’s death.
Children (under 12 years) are tracked separately, transitioning to adults at age 12.
4. Resource Management
Tribes consume food and water from their environment, requiring 0.5 units per member per update.
Resources regenerate seasonally: spring boosts food and water, summer reduces water, autumn reduces food, and winter depletes both.
If resources fall below a scarcity threshold (default 0.6), tribes migrate to better locations, impacting health and stress (0–100 scale).
5. Battles and Tribe Splits
Nearby tribes can engage in battles, with strength based on adult males (aged 16+). The winner captures females, while the loser loses males.
Overcrowding or high stress can trigger tribe splits, creating new tribes at least 10 grid units away from the original.
6. Environmental Seasons
The game cycles through four seasons (spring, summer, autumn, winter) every three months, affecting resource availability and survival rates.
Each season alters food and water levels, influencing tribe behavior and stress.
7. Player Interaction
Players can click the map to move their tribe to a new location.
Settings panel allows customization of initial population (min 2), male/female counts, max tribe size, reproduction/infant/maternal mortality rates, and scarcity threshold.
8. Multi-Language Support
The game supports Turkish, English, Arabic, and Chinese, with a dropdown menu in the top-right corner for language selection.
All UI text, messages, and tooltips dynamically update based on the chosen language.
9. Game History and Statistics
Tracks tribe histories, including births, deaths, splits, battles, and extinction reasons.
Displays real-time stats (year, month, season, total population, gender counts, children, births, deaths).
Offers options to download tribe logs (TXT), population charts (PNG), and share game results via clipboard.
10. Game Over Conditions
The game ends immediately when all tribes are extinct, triggered by the last member’s death (e.g., last man or last woman dying) or extreme stress/resource scarcity.
A game-over screen shows tribe history, duration, final tribe count, and reason for extinction, with options to restart or share.
How It Began (Detailed)
The concept emerged from a curiosity about simulating real human behaviors in a simple grid-based system, contrasting with Conway’s Game of Life’s abstract cells. Initial experiments with ChatGPT 4 helped prototype basic mechanics, but limitations in complexity and speed prompted a shift to Grok 3. Using Grok 3, I conceptualized the game’s features (world generation, tribal dynamics, reproduction, etc.), requested code generation, tested outputs, and iterated rapidly. The entire codebase—HTML, CSS, and JavaScript—was rewritten in a day, showcasing Grok 3’s capabilities. I never manually coded; instead, I focused on ideation, testing, and refining via Grok’s responses.
How to Deploy
To make "Adam and Eve: The Beginning" available online, follow these steps:
Upload the code to a GitHub repository:
Initialize a Git repository locally, add your files, commit, and push to GitHub (see instructions below or GitHub documentation).
Use GitHub Pages, Netlify, or Vercel to deploy the game online:
For GitHub Pages: Go to your repository settings, enable Pages, and select the main branch as the source. The game will be live at https://<username>.github.io/<repo-name>/.
For Netlify/Vercel: Connect your GitHub repository, configure automatic deployment, and the game will be accessible at a custom URL (e.g., https://<game-name>.netlify.app or https://<game-name>.vercel.app).
Development and Contribution
This project was exclusively developed using Grok 3 by xAI, leveraging its AI-driven code generation to prototype and refine the game. I conceptualized features and functions, while Grok 3 handled coding, testing, and iteration based on my feedback. No manual coding was performed; the process relied on ideation, testing, and iterative requests to Grok 3.
"Adam and Eve: The Beginning" is a fun, open-source side project, and anyone can download it to play, study, or improve it. We encourage you to fork the repository, experiment with the code, and share your enhancements with the community. Referrals are welcomed—feel free to share this project with others, post it on forums, social media, or gaming communities to spread the word and attract contributors.
Contributing
We warmly welcome contributions to enhance "Adam and Eve: The Beginning"! Here’s how you can contribute:
Fork the Repository:
Create your own copy of this repository on GitHub.
Create a New Branch:
Use the following command to create a branch for your changes:
bash
git checkout -b feature/your-feature-name
Make Changes and Commit:
Edit the code, add features, or fix bugs. Stage your changes and commit:
bash
git add .
git commit -m "Add your feature description or bug fix"
Push to Your Fork:
Push your changes to your forked repository:
bash
git push origin feature/your-feature-name
Submit a Pull Request:
Open a pull request on the main repository’s GitHub page. We’ll review and merge your changes.
Before Contributing:
Please open an issue on GitHub to discuss your idea or bug report. This ensures alignment with the project’s goals and prevents duplicate efforts.
As this is a beta release, feedback on bugs, usability issues, performance, and new features is highly valuable. Use GitHub Issues to report problems or suggest improvements.
Technical Details
Languages and Tools: HTML5, CSS3, JavaScript (ES6+), Chart.js (for population charts).
Dependencies: No external libraries except Chart.js (loaded via CDN).
File Structure:
index.html: Main HTML file with game UI and canvas.
style.css: CSS for layout, styling, and responsiveness.
Script (inline in HTML): JavaScript for game logic, world generation, and tribal simulation.
License
This project is licensed under the MIT License. See the LICENSE file for details. This license allows you to use, modify, and distribute the code freely, provided you include the original copyright notice and this permission notice in all copies.
Acknowledgments
Grok 3 by xAI: Special thanks for enabling the rapid development and iteration of this game through AI-driven code generation.
Inspiration: Conway’s Game of Life and survival simulation concepts for sparking the initial idea.
Community: Gratitude to early testers and contributors who help shape this project.
Known Issues (Beta)
Some UI elements may overlap on smaller screens (e.g., mobile devices).
Occasional performance lag with large populations or complex world generation.
Multi-language text alignment may need refinement in certain languages.
Report issues via GitHub Issues for prioritization in future updates.
Future Plans
Add mobile responsiveness for a seamless experience on all devices.
Introduce more environmental challenges (e.g., natural disasters, diseases).
Enhance graphics with animations or SVG-based tribe markers.
Expand language support and improve localization.
Optimize performance for larger-scale simulations.
Contact
For questions, feedback, or collaboration, please open an issue on GitHub or contact the maintainer via email (if provided in your profile). Follow the project on GitHub for updates! Referrals are welcomed—share this project on forums, social media, or gaming communities to spread the word and attract contributors.
