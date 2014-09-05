chefdk
------

A container to use ChefDK tools easily in a dev environment

Usage
-----

Create and use aliases for the ChefDK tools:

    alias knife="docker run --rm -t -i -e OPSCODE_USER=\$USER -v \$(pwd):/data chefdk knife"
    
    knife status

