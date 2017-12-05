deployd-docs
============

documentation for the deployd nodejs REST API Framework www.deployd.com



Workflow
---------------

    ## Quick and easy step.
    Fork this repo
    Create a github.io page from the >settings of the repository.
    Browse docs pages at your-github-username.github.io/the-repo-name
    Modify the pages , save and browse the changes
    
    Once ready to merge create a pull request. That is it. 



    ## To install on your pc

    # clone this repository. From 'docs'  - folder,
    npm install
    
    # make sure http-server is installed by (you can use your favour http server)
    # npm install -g http-server

    # start a simple http server
    http-server _site &

    # open browser and go to http://localhost:8080/


    # open another terminal
    node staticGen.js
    # change the docs files, and test the out until it is ok


    # push to git remote origin gh-pages by
    node bin/gen-gh-pages.js


Then, go to github and create a pull request to deployd/docs gh-pages branch.

Thanks
