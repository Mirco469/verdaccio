# verdaccio

The content of htpasswd was generated after running `npm adduser --registry http://localhost:4873/` and adding a user with username test, password test and email test@test.com

At some point the password changed because the algorithm used changed from "crypt" to "bcrypy" following a warning in the console (algorithm changed in config.yaml)

Set max_users: -1 to disable new user registrations

Set declaration = true in mynpmpackage to tell typescript to generate types

Value for \_auth in .npmrc file is the result of `echo -n '<username>:<password>' | base64`. `-n` avoid the creation of a newline while generating the base64

Use `npm update mynpmpackage-mirco` on the testpackage (the package that uses mynpmpackage) to update the dependency after a new version is published. Otherwiser even running npm install will leave us with the already downloaded version even if a new one is available.

When running npm `login --registry http://localhost:4873/` the result is written inside the .npmrc C:\Users\<nome-utente>\.npmrc.
Here we can find \_auth and \_authToken (for some reason the \_auth generated from the login was different from the echo base64. I did not try to use the login \_auth in place of the base64 to see if it workend anyway)
