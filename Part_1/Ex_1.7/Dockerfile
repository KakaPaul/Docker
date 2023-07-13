# Starting from Ubuntu image
FROM ubuntu:20.04

# Install curl into the Ubuntu image
#RUN apk --no-cache add curl
RUN apt-get update && apt-get install -y curl && apt-get clean

# Use /usr/src/app as our working directory.
WORKDIR	/usr/src/app

# Copy the missing_dependencies.sh file from this location to /usr/src/app/ creating /usr/src/app/missing_dependencies.sh
COPY missingDependencies.sh /usr/src/app/missingDependencies.sh

# Alternatively, if we skipped chmod earlier, we can add execution permissions during the build.
RUN chmod +x /usr/src/app/missingDependencies.sh

# When running Docker run the command will be ./missing_dependencies.sh
CMD sh missingDependencies.sh
