---
layout: page
title: Sudoku Solver
permalink: /portfolio/sudoku/
comments: true
---

<div class='add-pad'>
	<p><a class='res-link' href='http://codepen.io/angelariggs/full/JdpqGW/' target='blank'>Launch Sudoku on CodePen</a></p>

	<div id='sudoku-embed'>
		<p data-height="300" data-theme-id="17586" data-slug-hash="JdpqGW" data-default-tab="result" data-user="angelariggs" class='codepen'>See the Pen <a href='http://codepen.io/angelariggs/pen/JdpqGW/'>Sudoku Solver</a> by Angela Riggs (<a href='http://codepen.io/angelariggs'>@angelariggs</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
		<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
	</div>

	<h2 class='project-sec-header'>About Sudoku Solver</h2>
	<p>Sudoku Solver was a small-group project, assigned as part of Portland Code School's JavaScript Immersion coursework. This was really the first web app that we built from scratch, having to concept and create the functionality ourselves.</p>
	<p>Sudoku Solver was presented as a multi-day assignment, so it was also one of the few projects that offered the chance to refactor and refine code during class.</p>

	<h2 class='project-sec-header'>Technical Specs</h2>
	<p>Our initial version of the Sudoku Solver was display-only, rather than interactive. We figured out the mathematic formula that we needed in order to display the grid layout, as well as the placement of the numbers and spaces. Once we figured out the formula, the biggest challenge was reconciling an 81-number grid with a zero-index system!</p>
	<p>Our goal for the second iteration was to build a functional Sudoku grid. We used constructors to create the squares, rows, columns, & blocks. It may seem redundant to define functions for both rows and columns - after all, creating one results in the other. But solving a Sudoku puzzle requires knowing all numbers in an individual square's row, its column, and its 3x3 block.</p>
	<!-- <p>Our knowledge of <i>this</i> came into play for creating this functional grid. FILL IN LATER. INCLUDE JUNE18 SUDOKU FILE</p> -->

	<!-- <h2 class='project-sec-header'>Responsibilities</h2>
	<p>The Sudoku Solver was completed as a pair programming project, with myself and <a href='https://www.linkedin.com/pub/morgan-leonard/4/b78/823'>Morgan</a>. </p> -->
</div>