---
keywords: fastai
title: Developing Algorithms
toc: true 
badges: true
comments: true
nb_path: _notebooks/2022-12-06-Developing-Algorithms.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-12-06-Developing-Algorithms.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Algorithms can be written in different ways and still accomplish the same tasks.
Algorithms that look similar often yield differnet outputs.
To solve the same problem, many different algorithms can be used.</p>
<p>Therefore, algorithms are very important for programmers, and today we're going to explore how to determine the outcome of algorithms, how to deteremine the output of similar algorithms, how to edit existing algorithms, and how to develop our own algorithms.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Determine-the-outcome-of-algorithms">Determine the outcome of algorithms<a class="anchor-link" href="#Determine-the-outcome-of-algorithms"> </a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><strong>Consider the following algorithm.</strong></p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">mystery</span><span class="p">(</span><span class="n">num</span><span class="p">,</span> <span class="n">num2</span><span class="p">):</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">num</span> <span class="o">%</span> <span class="n">num2</span> <span class="o">==</span> <span class="mi">0</span><span class="p">):</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;True&quot;</span><span class="p">)</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;False&quot;</span><span class="p">)</span>

<span class="n">mystery</span><span class="p">(</span><span class="mi">20</span><span class="p">,</span> <span class="mi">4</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>True
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ol>
<li>What does the algorithm do? Please explain in words.</li>
<li>What if I put in 30 as num and 4 as num2. What would be the output?</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Determine-the-outcome-of-similar-algorithms">Determine the outcome of similar algorithms<a class="anchor-link" href="#Determine-the-outcome-of-similar-algorithms"> </a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>What is the output of this algorithm?</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span> <span class="o">=</span> <span class="mi">95</span>
<span class="k">if</span> <span class="p">(</span><span class="n">temp</span> <span class="o">&gt;=</span> <span class="mi">90</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;it is too hot outside&quot;</span><span class="p">)</span>
<span class="k">else</span><span class="p">:</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">temp</span> <span class="o">&gt;=</span> <span class="mi">65</span><span class="p">):</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;I will go outside&quot;</span><span class="p">)</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;it is too cold outside&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>What is the output of this algorithm? it looks similar but the output is different!</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">temp</span> <span class="o">=</span> <span class="mi">95</span>
<span class="k">if</span> <span class="p">(</span><span class="n">temp</span> <span class="o">&gt;=</span> <span class="mi">90</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;it is too hot outside&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="p">(</span><span class="n">temp</span> <span class="o">&gt;=</span> <span class="mi">65</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;i will go outside&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="p">(</span><span class="n">temp</span> <span class="o">&lt;</span> <span class="mi">65</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;it is too cold outside&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Editing-Algorithms">Editing Algorithms<a class="anchor-link" href="#Editing-Algorithms"> </a></h3><p>Task: Please edit the algorithm above to have it yield the same results as the previous algorithm! (no matter what temp you put in)</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Developing-Algorithms">Developing Algorithms<a class="anchor-link" href="#Developing-Algorithms"> </a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>To develop algorithms, we first need to understand what the question is asking. Then, think about how you would approach it as a human and then try to find what pattern you went through to arrive at the answer. Apply this to code, and there you have it! An algorithm!</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Let's say you wanted to sum up the first five integers. How would you do this in real life?
Your thought process would probably be:</p>
<ul>
<li>The sum of the first integer is 1. </li>
<li>Then, increase that integer by 1. I now add 2 to my existing sum (1). My new sum is 3.</li>
<li>Repeat until I add 5 to my sum.
The resulting sum is 15.</li>
</ul>
<p>Now let's translate this into code.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">sum</span> <span class="o">=</span> <span class="mi">0</span> <span class="c1"># start with a sum of 0</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span> <span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">6</span><span class="p">):</span> <span class="c1"># you will repeat the process five times for integers 1-5</span>
    <span class="nb">sum</span> <span class="o">=</span> <span class="nb">sum</span> <span class="o">+</span> <span class="n">i</span> <span class="c1"># add the number to your sum</span>
<span class="nb">print</span><span class="p">(</span><span class="nb">sum</span><span class="p">)</span> <span class="c1"># print the result</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>15
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Task: Write an algorithm in python that sums up the first 5 odd integers. You can use the following code as a starter.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">sum</span> <span class="o">=</span> <span class="mi">0</span>
<span class="n">counter</span> <span class="o">=</span> <span class="mi">0</span> <span class="c1"># is counter max to use? so it can be whatever &gt; 9?</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span> <span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">10</span><span class="p">):</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">i</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">1</span><span class="p">):</span>
        <span class="nb">sum</span> <span class="o">=</span> <span class="nb">sum</span> <span class="o">+</span> <span class="n">i</span>
        <span class="n">counter</span> <span class="o">=</span> <span class="n">counter</span> <span class="o">+</span> <span class="mi">1</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">counter</span> <span class="o">&gt;=</span> <span class="mi">5</span><span class="p">):</span>
        <span class="k">break</span>
<span class="nb">print</span><span class="p">(</span><span class="nb">sum</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>75
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Homework">Homework<a class="anchor-link" href="#Homework"> </a></h3><p>Create an algorithm that will start with any positive integer n and display the full sequence of numbers that result from the Collatz Conjecture. The COllatz Conjecture is as follows:</p>
<ol>
<li>start with any positive integer</li>
<li>if the number is even, divide by 2</li>
<li>if the number is odd, multiply by 3 and add 1</li>
<li>repeat steps 2 and 3 until you reach 1</li>
</ol>
<p>Example: if the starting number was 6, the output would be 6, 3, 10, 5, 16, 8, 4, 2, 1</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">calculateNumber</span><span class="p">(</span><span class="n">num</span><span class="p">):</span>
    <span class="n">result</span> <span class="o">=</span> <span class="n">num</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">num</span> <span class="o">==</span> <span class="mi">0</span><span class="p">):</span>
        <span class="k">return</span> <span class="p">[]</span>

    <span class="n">result_list</span> <span class="o">=</span> <span class="p">[</span><span class="n">result</span><span class="p">]</span>
    <span class="k">while</span> <span class="n">result</span> <span class="o">!=</span> <span class="mi">1</span><span class="p">:</span>
        <span class="k">if</span> <span class="p">(</span><span class="n">result</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">0</span><span class="p">):</span> <span class="c1"># use mod = remander = 0 -&gt; even. 1 = odd</span>
            <span class="n">result</span> <span class="o">=</span> <span class="n">result</span> <span class="o">/</span> <span class="mi">2</span>
        <span class="k">else</span><span class="p">:</span>
            <span class="n">result</span> <span class="o">=</span> <span class="n">result</span> <span class="o">*</span> <span class="mi">3</span> <span class="o">+</span> <span class="mi">1</span>
        <span class="n">result_list</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="nb">int</span><span class="p">(</span><span class="n">result</span><span class="p">))</span> <span class="c1"># appends the result to a string of results so it can be printed later</span>
    <span class="k">return</span> <span class="n">result_list</span>
    
<span class="c1"># Input function </span>
<span class="n">s</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span>
<span class="k">while</span> <span class="p">(</span><span class="n">s</span> <span class="o">!=</span> <span class="s2">&quot;q&quot;</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n</span><span class="s2">Enter a number or type &#39;q&#39; to quit.&quot;</span><span class="p">)</span>
    <span class="n">s</span> <span class="o">=</span> <span class="nb">input</span><span class="p">()</span>
    <span class="k">try</span><span class="p">:</span>
        <span class="k">if</span> <span class="n">s</span> <span class="o">!=</span> <span class="s2">&quot;q&quot;</span><span class="p">:</span>
            <span class="n">num</span> <span class="o">=</span> <span class="p">(</span><span class="nb">int</span><span class="p">(</span><span class="n">s</span><span class="p">))</span>
            <span class="n">resultFinal</span> <span class="o">=</span> <span class="n">calculateNumber</span><span class="p">(</span><span class="n">num</span><span class="p">)</span>
            <span class="nb">print</span><span class="p">(</span><span class="n">resultFinal</span><span class="p">)</span>
    <span class="k">except</span> <span class="ne">ValueError</span><span class="p">:</span>
        <span class="nb">print</span> <span class="p">(</span><span class="s2">&quot;Invalid input.&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>
Enter a number or type &#39;q&#39; to quit.
[6, 3, 10, 5, 16, 8, 4, 2, 1]

Enter a number or type &#39;q&#39; to quit.
[100, 50, 25, 76, 38, 19, 58, 29, 88, 44, 22, 11, 34, 17, 52, 26, 13, 40, 20, 10, 5, 16, 8, 4, 2, 1]

Enter a number or type &#39;q&#39; to quit.
[456, 228, 114, 57, 172, 86, 43, 130, 65, 196, 98, 49, 148, 74, 37, 112, 56, 28, 14, 7, 22, 11, 34, 17, 52, 26, 13, 40, 20, 10, 5, 16, 8, 4, 2, 1]

Enter a number or type &#39;q&#39; to quit.
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 
