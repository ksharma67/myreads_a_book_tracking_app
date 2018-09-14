<h1>MyReads Project</h1>
<p>This project is a part of the final assessment for Udacity's React Fundamentals course. The goal of this project is to create a personal book tracker app to track the books which you are "Currently Reading", "Want to read", and "Already read"</p>
<p>Use <a href="https://github.com/facebookincubator/create-react-app">Create React App</a> to bootstrap the project.</p>
<h2><a id="user-content-tldr" class="anchor" aria-hidden="true" href="#tldr"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>TL;DR</h2>
<p>To get started developing right away:</p>
<ul>
<li>install all project dependencies with <code>npm install</code></li>
<li>start the development server with <code>npm run start</code></li>
</ul>
<h2><a id="user-content-what-youre-getting" class="anchor" aria-hidden="true" href="#what-youre-getting"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>What You're Getting</h2>
<div class="highlight highlight-source-shell"><pre>├── README.md - This file.
├── SEARCH_TERMS.md <span class="pl-c"><span class="pl-c">#</span> The whitelisted short collection of available search terms for you to use with your app.</span>
├── package.json <span class="pl-c"><span class="pl-c">#</span> npm package manager file. It's unlikely that you'll need to modify this.</span>
├── public
│   ├── favicon.ico <span class="pl-c"><span class="pl-c">#</span> React Icon, You may change if you wish.</span>
│   └── index.html <span class="pl-c"><span class="pl-c">#</span> DO NOT MODIFY</span>
└── src
    ├── App.css <span class="pl-c"><span class="pl-c">#</span> Styles for your app. Feel free to customize this as you desire.</span>
    ├── App.js <span class="pl-c"><span class="pl-c">#</span> This is the root of your app. Contains static HTML right now.</span>
    ├── App.test.js <span class="pl-c"><span class="pl-c">#</span> Used for testing. Provided with Create React App. Testing is encouraged, but not required.</span>
    ├── BooksAPI.js <span class="pl-c"><span class="pl-c">#</span> A JavaScript API for the provided Udacity backend. Instructions for the methods are below.</span>
    ├── icons <span class="pl-c"><span class="pl-c">#</span> Helpful images for your app. Use at your discretion.</span>
    │   ├── add.svg
    │   ├── arrow-back.svg
    │   └── arrow-drop-down.svg
    ├── components
    <span class="pl-k">|</span>	├── AddBook.js
    <span class="pl-k">|</span>	├── Book.js
    <span class="pl-k">|</span>	├── ErrorPage404.js
    <span class="pl-k">|</span>	├── Main.js
    <span class="pl-k">|</span>	├── Search.js
    <span class="pl-k">|</span>	├── Shelf.js
    <span class="pl-k">|</span>	├── ShelfRow.js
    <span class="pl-k">|</span>	└── Title.js
    ├── img
    <span class="pl-k">|</span>	└── no_cover_thumb.gif
    ├── index.css <span class="pl-c"><span class="pl-c">#</span> Global styles. You probably won't need to change anything here.</span>
    └── index.js <span class="pl-c"><span class="pl-c">#</span> You should not need to modify this file. It is used for DOM rendering only.</span></pre></div>
<h2><a id="user-content-backend-server" class="anchor" aria-hidden="true" href="#backend-server"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Backend Server</h2>
<p>To simplify your development process, we've provided a backend server for you to develop against. The provided file <a href="/prabhuvashwin/my-reads-book-app/blob/master/src/BooksAPI.js"><code>BooksAPI.js</code></a> contains the methods you will need to perform necessary operations on the backend:</p>
<ul>
<li><a href="#getall"><code>getAll</code></a></li>
<li><a href="#update"><code>update</code></a></li>
<li><a href="#search"><code>search</code></a></li>
</ul>
<h3><a id="user-content-getall" class="anchor" aria-hidden="true" href="#getall"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>getAll</code></h3>
<p>Method Signature:</p>
<div class="highlight highlight-source-js"><pre><span class="pl-en">getAll</span>()</pre></div>
<ul>
<li>Returns a Promise which resolves to a JSON object containing a collection of book objects.</li>
<li>This collection represents the books currently in the bookshelves in your app.</li>
</ul>
<h3><a id="user-content-update" class="anchor" aria-hidden="true" href="#update"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>update</code></h3>
<p>Method Signature:</p>
<div class="highlight highlight-source-js"><pre><span class="pl-en">update</span>(book, shelf)</pre></div>
<ul>
<li>book: <code>&lt;Object&gt;</code> containing at minimum an <code>id</code> attribute</li>
<li>shelf: <code>&lt;String&gt;</code> contains one of ["wantToRead", "currentlyReading", "read"]</li>
<li>Returns a Promise which resolves to a JSON object containing the response data of the POST request</li>
</ul>
<h3><a id="user-content-search" class="anchor" aria-hidden="true" href="#search"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>search</code></h3>
<p>Method Signature:</p>
<div class="highlight highlight-source-js"><pre><span class="pl-en">search</span>(query, maxResults)</pre></div>
<ul>
<li>query: <code>&lt;String&gt;</code></li>
<li>maxResults: <code>&lt;Integer&gt;</code> Due to the nature of the backend server, search results are capped at 20, even if this is set higher.</li>
<li>Returns a Promise which resolves to a JSON object containing a collection of book objects.</li>
<li>These books do not know which shelf they are on. They are raw results only. You'll need to make sure that books have the correct state while on the search page.</li>
</ul>
<h2><a id="user-content-important" class="anchor" aria-hidden="true" href="#important"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>
