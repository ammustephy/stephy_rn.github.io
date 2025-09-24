/* Dark theme by default */
:root {
    --bg-color: #121212;
    --text-color: #e0e0e0;
    --accent-color: #64b5f6; /* Blue for links/buttons */
    --card-bg: #1e1e1e;
    --border-color: #333;
}

@media (prefers-color-scheme: light) {
    :root {
        --bg-color: #ffffff;
        --text-color: #333333;
        --accent-color: #1976d2;
        --card-bg: #f5f5f5;
        --border-color: #ddd;
    }
}

body {
    font-family: 'Arial', sans-serif;
    background-color: var(--bg-color);
    color: var(--text-color);
    margin: 0;
    padding: 0;
    line-height: 1.6;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}

header {
    background-color: var(--card-bg);
    text-align: center;
    padding: 40px 20px;
}

h1, h2, h3 {
    color: var(--accent-color);
}

section {
    margin-bottom: 40px;
}

ul {
    list-style-type: disc;
    padding-left: 20px;
}

.experience-item {
    margin-bottom: 20px;
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
}

.project-card {
    background-color: var(--card-bg);
    border: 1px solid var(--border-color);
    border-radius: 8px;
    padding: 20px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    transition: transform 0.3s ease;
}

.project-card:hover {
    transform: translateY(-5px);
}

.project-card img {
    width: 100%;
    height: auto;
    border-radius: 4px;
    margin-bottom: 10px;
}

.btn {
    display: inline-block;
    background-color: var(--accent-color);
    color: var(--bg-color);
    padding: 10px 15px;
    text-decoration: none;
    border-radius: 4px;
    transition: background-color 0.3s;
}

.btn:hover {
    background-color: darken(var(--accent-color), 10%);
}

footer {
    text-align: center;
    padding: 20px;
    background-color: var(--card-bg);
    border-top: 1px solid var(--border-color);
}

a {
    color: var(--accent-color);
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
}

/* Responsive adjustments */
@media (max-width: 768px) {
    .projects-grid {
        grid-template-columns: 1fr;
    }
}
