# page-modern.css
skipper pour une page moderne Obsidian

/* Modern Obsidian Aesthetics - Glassmorphism & Gradients */

/* --- Typography & Headers --- */
.theme-dark,
.theme-light {
    --h1-gradient: linear-gradient(90deg, #7c3aed, #e50505);
    --h2-color: #e50505;
    /* Rose */
    --h3-color: #7c3aed;
    /* Violet */
    --link-color: #7c3aed;
}

/* H1 - En-tête de page Moderne */
h1 {
    background: var(--h1-gradient);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-weight: 800 !important;
    font-size: 2.5em !important;
    text-align: center;
    margin-bottom: 2rem !important;
    padding-bottom: 1rem;
    border-bottom: 2px solid rgba(124, 58, 237, 0.2);
}

/* H2 - Section avec Icône */
h2 {
    color: var(--h2-color) !important;
    font-weight: 700 !important;
    font-size: 1.8em !important;
    margin-top: 2rem !important;
    display: flex;
    align-items: center;
}

h2::before {
    content: '◈';
    /* Icône diamant moderne */
    margin-right: 10px;
    font-size: 0.8em;
    color: var(--h2-color);
    opacity: 0.8;
}

/* H3 - Sous-titre avec Icône */
h3 {
    color: var(--h3-color) !important;
    font-weight: 600 !important;
    font-size: 1.4em !important;
    margin-top: 1.5rem !important;
    display: flex;
    align-items: center;
}

h3::before {
    content: '❖';
    /* Icône losange floral */
    margin-right: 8px;
    font-size: 0.8em;
    color: var(--h3-color);
    opacity: 0.8;
}

/* H4 - Label Technique */
h4 {
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-size: 0.85em !important;
    font-weight: 600 !important;
    margin-top: 1.5rem !important;
    border-bottom: 1px solid var(--background-modifier-border);
    padding-bottom: 0.5rem;
}

/* --- Liens & Checkbox --- */

/* Liens Externes avec petite flèche */
a.external-link {
    text-decoration: none;
    color: var(--link-color);
}

a.external-link::after {
    content: ' ↗';
    font-size: 0.8em;
    opacity: 0.7;
}

/* Checkbox Modernes (Rondes) */
input[type="checkbox"] {
    -webkit-appearance: none;
    appearance: none;
    width: 1.1em;
    height: 1.1em;
    border: 1px solid var(--text-muted);
    border-radius: 50%;
    /* Rond parfait */
    margin-right: 0.5em;
    position: relative;
    top: 2px;
    transition: all 0.2s ease;
    cursor: pointer;
}

input[type="checkbox"]:checked {
    background: var(--h2-color);
    border-color: var(--h2-color);
    /* Petite coche blanche */
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='white' stroke-width='3' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpolyline points='20 6 9 17 4 12'%3E%3C/polyline%3E%3C/svg%3E");
    background-size: 70%;
    background-position: center;
    background-repeat: no-repeat;
}

/* --- Glassmorphism Callouts (Compatible) --- */
.callout {
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 12px;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.callout:hover {
    transform: translateY(-2px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
}

/* Styles spécifiques pour le Dashboard si utilisé */
.callout[data-callout="note"] {
    background: linear-gradient(135deg, rgba(124, 58, 237, 0.1), rgba(229, 5, 5, 0.1));
    border-left-color: var(--h3-color);
}

/* Mise en page grille (Grid) */
.note-container {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
}

.note-item {
    flex: 1 1 300px;
}
