## Authentication to Github repo

Make sure you have the following in ~/.m2/settings.xml to allow publishing the package to Github repo.

<servers>
    <server>
       <id>rubicon_github</id>
       <username>username</username>
       <password>"Github Personal Access Token (Classic)"</password>
    </server>
</servers>

## Building presto-hive

cd presto-hive
../mvnw clean install deploy -Dmaven.test.skip=true

This will build presto-hive and publish a new SNAPSHOT version on Fentik rubicon repo presto.
