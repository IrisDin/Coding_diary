# 🕸 Web devlopment

crete a new branch

git checkout gh-pages

git merge main

git checkout main



\<em>emphasis\<em>

em{

font-style: normal;

text-decoration: underline;

}

```
// html style quick reference

    <!DOCTYPE html>
    <html lang="en">
       
       <head>
           <!-- metadata that gives the info about the author -->
           <meta charset="UTF-8">
           <meta name="author" content="Iris Ding">
           <title>Sherlock Holmes</title>
            <!-- link the css style -->
            <link rel="stylesheet" href="css/style.css">
       </head>
       
       <body>
           <!-- creating top-level heading -->
           <h1>Sherlock Holmes</h1>
            <!-- insert image -->
           <img src="img/sherlock.jpg" alt="the picture of detective sherlock Holmes"/>
           <p>
               Description of the character :
           </p>
               <p>
               <!-- insert hyperlink -->
               <!-- insert short paragraph with description -->
               <a href="https://www.britannica.com/topic/Sherlock-Holmes">Sherlock Holmes</a>
               is a character from the British author Sir Arthur Conan Doyl.
               Sherlock was ...
               </p>
           <p>The reason why I admire Sherlock Holmes:</p>
           <p>
           I am especially admired with his following characteristics:
           </p>
           <!-- create unordered list -->
           <ul>
               <li class="sherlock_personality">
                   Observant
               </li>
               <li>Intelligent</li>
               <li>Strong mind</li>
               <li>Loyal</li>
           </ul>
       </body>
    </html>
```

```
// css quick reference

body{
    font-size: 16px;
    font-family: 'Helvetica Neue',Helvetica, Arial,sans-serif;
}

/* change the style of paragraph */
p{
    line-height: 1.5;
}
/* change the style of the image */
img{
    max-height: 400px;
    border-radius: 10px;
}

/* use the class selector to change the specific style of a class */
.sherlock_personality {
    color:rgb(47, 92, 255);
}
```



