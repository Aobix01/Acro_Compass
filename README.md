# Acropolis Campus Navigator

A beginner-friendly campus navigation system created for the
Acropolis Institute of Technology and Research, Indore.

## Features

- Select current location
- Select destination
- Find shortest route
- Dijkstra shortest-path algorithm
- SVG campus map
- Route visualization
- Distance calculation
- Walking-time estimation
- Turn-by-turn directions
- Popular destinations
- Swap locations
- Clear route
- Responsive mobile design

## Project Structure

acropolis-campus-navigator/
│
├── index.html
├── style.css
├── script.js
└── README.md

## How to Run

No backend is required.

Simply open:

index.html

in Google Chrome, Microsoft Edge, Firefox, or another modern browser.

You can also use VS Code with the Live Server extension.

## How Routing Works

The campus is represented as a graph.

Each campus location is a node.

For example:

Main Gate → Reception → Block 1 → Block 2 → Library

The connections between locations are edges.

Each edge has a distance.

Dijkstra's algorithm checks these distances and finds the
shortest route between the selected starting location and
destination.

## Adding a New Location

Add the location to the `locations` object in `script.js`.

Example:

"lab-1": {
    name: "Computer Lab 1",
    x: 400,
    y: 300,
    type: "Laboratory",
    description: "Computer laboratory for practical sessions."
}

Then add its connections to the `graph`.

Example:

"lab-1": {
    "block-2": 80,
    library: 120
}

The location also needs a corresponding SVG element in
`index.html`.

## Changing the Campus Map

The map is an SVG.

The SVG uses coordinates from:

x = horizontal position

y = vertical position

For example:

<circle cx="500" cy="300" r="10"/>

Changing `cx` moves the location horizontally.

Changing `cy` moves it vertically.

The coordinates in `locations` should match the visual
position of the location on the SVG.

## Important

This prototype uses a custom simplified campus map.

The distances are demonstration values and should be replaced
with measured campus distances when an official campus map or
verified campus measurements are available.
