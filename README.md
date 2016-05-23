cf push aspnetcoreapp -m 1g -b https://github.com/cloudfoundry-community/asp.net5-buildpack.git --no-start
cf enable-diego aspnetcoreapp
cf start aspnetcoreapp