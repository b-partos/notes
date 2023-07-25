# A Collection of usefule maven commands discovered through work

## Collect the the transitive closure of the dependencies of a pom as jars

The maven **`dependency`** plugin provides the **`copy-dependencies`** goal. By default this collects the depencencies into the **`target/dependency`** folder of the project.

Just invoke:
```
mvn dependency:copy-dependencies
```
The optional parameter *`classifier`* can be used to copy the source jar-s instead:
```
mvn dependency:copy-dependencies -Dclassifier=sources
```

See the [plugin](https://maven.apache.org/plugins/maven-dependency-plugin/) page for all parameters, including setting the target path.
