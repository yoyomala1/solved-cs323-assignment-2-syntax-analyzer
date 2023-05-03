Download Link: https://assignmentchef.com/product/solved-cs323-assignment-2-syntax-analyzer
<br>
The second assignment is to write a syntax analyzer. You may use any top-down parser such as a RDP,    a predictive recursive descent parser or a table driven predictive parser.

<strong> Hence, your assignment consists of the following tasks</strong>:

<ol>

 <li>Rewrite the grammar provided to remove any left recursion</li>

</ol>

(Also, use left factorization if necessary)

<ol start="2">

 <li>Use the <strong>lexer() </strong>generated in the assignment 1 to get the tokens</li>

 <li><strong>The parser should print to an output file the <u>tokens, lexemes</u> and the <u>production rules  used;</u> </strong></li>

</ol>

That is,<strong><u> first, write the token and lexeme found</u></strong>

Then,   <strong><u>print out all productions rules</u></strong> used for analyzing this token

Note:  – a simple way to do it is to have a “print statement” at the beginning of each function that will print                   the production rule.

– It would be a good idea to have a “switch” with the “print statement” so that you can turn it on or off. 4.<strong> Error handling:</strong> if a syntax error occurs, your parser should generate a meaningful error message, such as token, lexeme, line number, and error type etc.

Then, your program may exit or you may continue for further analysis.

<u>The bottom line is that your program must be able to parse the entire program if it is syntactically correct.</u>

<ol start="5">

 <li><strong><u> Turn in your assignment according to the specifications given in the project outline</u> </strong></li>

</ol>




<h1>                                                          Example</h1>

Assume we have the following statement

….more ….               a = b + c;               …. more ….




<strong><em><u>One possible output would be as follows</u></em>: </strong>

…. more….

<strong>Token: Identifier          Lexeme: a </strong>

&lt;Statement&gt; -&gt; &lt;Assign&gt;

&lt;Assign&gt; -&gt;  &lt;Identifier&gt;  = &lt;Expression&gt; ;

<strong>Token: Operator          Lexeme: = </strong>

<strong>Token: Identifier          Lexeme: b </strong>

&lt;Expression&gt; -&gt; &lt;Term&gt; &lt;Expression Prime&gt;

&lt;Term&gt; -&gt; &lt;Factor&gt; &lt;Term Prime&gt;

&lt;Factor&gt; -&gt; &lt;Identifier&gt;

<strong>Token:  Operator          Lexeme: + </strong>

&lt;Term Prime&gt; -&gt; 

&lt;Expression Prime&gt; -&gt; + &lt;Term&gt; &lt;Expression Prime&gt;

<strong>Token:  Identifier           Lexeme: c </strong>

&lt;Term&gt;  -&gt; &lt;Factor&gt; &lt;Term Prime&gt;

&lt;Factor&gt; -&gt; &lt;Identifier&gt;

<strong>Token: Separator           Lexeme: ; </strong>

&lt;Term Prime&gt; -&gt;       &lt;Expression Prime&gt; -&gt;  …. more…..