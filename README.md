<!DOCTYPE html>
<html>
<head>
<!-- <style>
  pre {
    background-color: black;
    color: white;
    padding: 10px;
    font-family: Consolas, Monaco, 'Andale Mono', 'Ubuntu Mono', monospace;
  }
</style> -->
</head>
<body>
<body>
  <h1>Regular Expression Tutorial: Matching Email Addresses</h1>

  <h2>Table of Contents</h2>
  <ol>
    <li><a href="#introduction">Introduction</a></li>
    <li><a href="#matching-username">Matching the Username</a></li>
    <li><a href="#matching-domain">Matching the Domain</a></li>
    <li><a href="#putting-it-together">Putting It All Together</a></li>
    <li><a href="#conclusion">Conclusion</a></li>
    <li><a href="#author">Author</a></li>
  </ol>

  <h2 id="introduction">1. Introduction</h2>

  <p>In this tutorial, we will learn how to create a regular expression that matches email addresses. Email addresses typically have the format <code>username@domain.com</code>. We will break down the regular expression into different components and explain each one.</p>

  <h2 id="matching-username">2. Matching the Username</h2>

  <p>The username part of an email address can consist of alphanumeric characters, dots, underscores, and hyphens. It cannot start or end with a dot and cannot have consecutive dots. We can use the following regular expression component to match the username:</p>

  <pre><code>^[a-zA-Z0-9]+([._-][a-zA-Z0-9]+)*</code></pre>

  <p>Explanation:</p>
  <ul>
    <li><code>^</code> asserts the start of the string.</li>
    <li><code>[a-zA-Z0-9]+</code> matches one or more alphanumeric characters.</li>
    <li><code>([._-][a-zA-Z0-9]+)*</code> matches zero or more occurrences of a dot, underscore, or hyphen followed by one or more alphanumeric characters.</li>
  </ul>

  <p>Example:</p>
  <ul>
    <li>Valid username: john.doe_123</li>
  </ul>

  <h2 id="matching-domain">3. Matching the Domain</h2>

  <p>The domain part of an email address typically consists of a domain name and a top-level domain (TLD). The domain name can consist of alphanumeric characters, dots, and hyphens. The TLD can consist of lowercase alphabets. We can use the following regular expression component to match the domain:</p>

  <pre><code>@[a-zA-Z0-9.-]+\.[a-z]+</code></pre>

  <p>Explanation:</p>
  <ul>
    <li><code>@</code> matches the "@" symbol.</li>
    <li><code>[a-zA-Z0-9.-]+</code> matches one or more alphanumeric characters, dots, or hyphens.</li>
    <li><code>\.[a-z]+</code> matches a dot followed by one or more lowercase alphabets.</li>
  </ul>

  <p>Example:</p>
  <ul>
    <li>Valid domain: example.com</li>
  </ul>

  <h2 id="putting-it-together">4. Putting It All Together</h2>

  <p>Now let's combine the username and domain components to form the complete regular expression for matching email addresses:</p>

  <pre><code id="tutorial-code">^[a-zA-Z0-9]+([._-][a-zA-Z0-9]+)*@[a-zA-Z0-9.-]+\.[a-z]+</code></pre>

  <button onclick="copyToClipboard()">Copy Code</button>

  <p>Explanation:</p>
  <ul>
    <li><code>^</code> asserts the start of the string.</li>
    <li><code>[a-zA-Z0-9]+([._-][a-zA-Z0-9]+)*</code> matches the username component.</li>
    <li><code>@</code> matches the "@" symbol.</li>
    <li><code>[a-zA-Z0-9.-]+\.[a-z]+</code> matches the domain component.</li>
  </ul>

  <p>Example:</p>
  <ul>
    <li>Valid email address: john.doe@example.com</li>
  </ul>

  <h2 id="conclusion">5. Conclusion</h2>

  <p>Congratulations! You have successfully created a regular expression to match email addresses. Regular expressions are powerful tools for pattern matching and can be used in various programming languages and text editors.</p>

  <p>Remember to test your regular expression with different email addresses to ensure it covers all possible cases.</p>

  <p>I hope this tutorial helps you understand the components of a regular expression for matching email addresses. Feel free to explore more complex patterns and adapt the concepts to match other patterns as well.</p>

  <h2 id="author">6. Author</h2>

  <p>This tutorial was written by Lionel Sanderson. You can find more tutorials and projects on [my GitHub profile](https://www.github.com/L10N37).</p>


</body>
</html>
