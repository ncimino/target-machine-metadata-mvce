# MVCE to test target machine metadata for C++ projects

This example came into existence while trying address some concerns about modules that publish metadata

# To test

Clean any previous runs _and the repository_ of this project:

    ./gradlew clean

Publish the dependency:

    ./gradlew :lib:publishAllPublicationsToLocalRepository
    
Build the dependent:

    ./gradlew :app:build
    
From here you can look at the metadata and even though we built on one OS it has the metadata from the other,
but this doesn't seem to cause any problems.
