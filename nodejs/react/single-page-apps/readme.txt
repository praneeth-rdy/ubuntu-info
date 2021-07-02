** When you host a react application on github with react routing, 
add the 404.html which is present in this base dir to the public folder of the project.
So that, when there is a force reload on a certain path server returns this 404.html,
which in turn, redirects to the necessary react route.
** After copying the 404.html, copy the script from index.html and place it in the index.html of your project's public folder
Note that the redirect script must be placed before your single page app script in your index.html file.


Refer to this url: https://github.com/rafgraph/spa-github-pages

1) 404.html is returned by the server at /repo/<other path>
2) This 404.html has a script which adds a ? to the url just after the index path of the app
3) Now the request is again sent to the server at /repo/?/<other path> and server returns index.html at this url
4) Now this index.html has a script which sends the user to the actual url without loading the page /repo/<other path>


So to do this:
1) Add the 404.html to the public folder of the app
2) Edit the index.html and add the required script

And....Boom!!!!