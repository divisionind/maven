# mvn-repo
This is a poor mans maven repo that I use for storing things I need.

## Adding libraries

You can add jars using this command:
`mvn install:install-file -DgroupId=YOUR_GROUP -DartifactId=YOUR_ARTIFACT -Dversion=YOUR_VERSION -Dfile=YOUR_JAR_FILE -Dpackaging=jar -DgeneratePom=true -DlocalRepositoryPath=.  -DcreateChecksum=true`

Once added, just track all the files and commit:
`git add -A . && git commit -m "added library x"`

Then push to the repo:
`git push origin repo`

## Using libraries

To use libraries, include this repo along with your others by adding the url:
`https://raw.githubusercontent.com/divisionind/maven/repo`