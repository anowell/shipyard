chefdk
------

A container to use ChefDK tools easily in a dev environment

Usage
-----

Create and use aliases for the ChefDK tools:

    for CMD in chef knife berks kitchen rubocop foodcritic; do
      alias $CMD="docker run --rm -t -i -e OPSCODE_USER=\$USER -v \$(pwd):/data chefdk $CMD";
    done

    # now use these tools similar to how you would if locally installed
    knife status
    berks version
    chef generate cookbook NAME
    
