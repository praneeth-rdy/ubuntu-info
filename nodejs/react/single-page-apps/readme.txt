** When you host a react application on github with react routing, 
add the 404.html which is present in this base dir to the public folder of the project.
So that, when there is a force reload on a certain path server returns this 404.html,
which in turn, redirects to the necessary react route.
** After copying the 404.html, copy the script from index.html and place it in the index.html of your project's public folder
Note that the redirect script must be placed before your single page app script in your index.html file.


Refer to this url: https://github.com/rafgraph/spa-github-pages