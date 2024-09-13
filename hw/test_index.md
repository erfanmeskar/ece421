---
title: test
layout: default
nav_order: 6
---

# Interactive SVG Example

This is an example of an interactive SVG that you can use in a Markdown file. Click on the shapes to interact!

<svg id="interactiveSVG" width="400" height="400" xmlns="http://www.w3.org/2000/svg">
    <!-- Circle element -->
    <circle id="circle1" class="svg-hover" cx="100" cy="100" r="50" stroke="black" stroke-width="2"/>
    
    <!-- Rectangle element -->
    <rect id="rect1" class="svg-hover" x="200" y="50" width="100" height="100" stroke="black" stroke-width="2"/>
    
    <!-- Text element -->
    <text id="text1" x="150" y="250" font-size="24" fill="black">Click the shapes!</text>
</svg>

<style>
    /* Style the SVG or individual elements */
    .svg-hover {
        fill: lightblue;
        cursor: pointer;
        transition: fill 0.3s;
    }

    .svg-hover:hover {
        fill: orange;
    }

    .svg-clicked {
        fill: green !important;
    }
</style>

<script>
    // Add interactivity to SVG elements

    // Circle interactivity
    document.getElementById('circle1').addEventListener('click', function () {
        this.classList.toggle('svg-clicked'); // Toggle fill color on click
        alert("Circle clicked!");
    });

    // Rectangle interactivity
    document.getElementById('rect1').addEventListener('click', function () {
        this.classList.toggle('svg-clicked'); // Toggle fill color on click
        alert("Rectangle clicked!");
    });

</script>