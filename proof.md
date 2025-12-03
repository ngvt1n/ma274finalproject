<style>
/*
latex.css
https://github.com/davidrzs/latexcss
MIT-License
*/

.katex {
  font: normal 1em KaTeX_Main, 'NewComputerModern10',serif;
}

.markdown-body {
  background-color: white;
  font-size: 13pt;
  transform: none;
}

.markdown-body {
	font-family: 'Comic Sans MS', serif;
	counter-reset: theorem;
    counter-reset: lemma;
	counter-reset: definition;
}

h1, h2, h3, h4, h5, h6 {
	border: none;
	font-weight: bold;
}

a, a:visited {
	color: #a00;
}

ul {
	list-style: disc;
}

/* Content Box */

.markdown-body {
	max-width: 720px;
	margin: 2em auto;
}

h1:first-of-type  {
	text-align: center;
	display: block;
}

/* Article Body */

.markdown-body {
	text-align: justify;
	-moz-hyphens: auto;
	-webkit-hyphens: auto;
	hyphens: auto;
  padding: 0 1em;
}

dl dd {
	/* center definitions (most useful for display equations) */
	text-align: center;
}

@media (min-width: 43.75em) {
  body {
    padding: 0;
  }
}


.theorem {
  counter-increment: theorem;
  display: block;
  margin: 12px 0;
  font-style: italic;
}
.theorem:before {
  content: "Theorem " counter(theorem) ". ";
  font-weight: bold;
  font-style: normal;
}
.lemma {
	 counter-increment: lemma;
    display: block;
    margin: 12px 0;
    font-style: italic;
}
.lemma:before {
	content: "Lemma " counter(lemma) ". ";
    font-weight: bold;
    font-style: normal;
}
.proof {
    display: block;
    margin: 12px 0;
    font-style: normal;
}
.proof:before {
    content: "Proof.";
    font-style: italic;
}
.proof:after {
    content: "\25FB";
    float:right;
}
.definition {
	 counter-increment: definition;
    display: block;
    margin: 12px 0;
    font-style: normal;
}
.definition:before {
 content: "Definition " counter(definition) ". ";
     font-weight: bold;
    font-style: normal;
}

.author {
	margin-top: 8px;
	margin-bottom: 8px;
  	font-variant-caps: small-caps;
  	text-align: center;
}
</style>

# Russell's Paradox and The Halting Problem

Let us start with a definition 

A number $n$ is called even if $n \% 2 = 0$. An odd number $m$ is odd if $m \%2 \neq 0$. Furthermore lets write $m$ as $m = 2q + 1$ and $n = 2p$ for $p, q ∈ \RR$ {.definition}

In order to prove the next theorem we will need the next Lemma which we will not prove. 

An even number plus an even number results in an even number.  {.lemma}

We can now come to our theorem. 

The sum of an odd number $m$ and an even number $n$ is always odd. {.theorem}

