Querying a favorite movie info through OMDB_API over network. Prerequisites: You need to obtain your personal API key from the OMDb API website in order to be able to use the tool. Once you have it, you can either pass it via --apikey argument, or if you don't wish to pass it every time, you can set it as an environment variable OMDB_API_KEY through ENV in Dockerfile.

Building an Image: First Build a image for our program by Dockerfile(we have a dockerfile in our repo). Edit the dockerfile and replace the movie name in CMD with your Movie name by "-t" tag and --tomatoes for . Then execute the folowing command to build an image.

Following are the arguments: optional arguments: -h, --help show this help message and exit -t T Movie title -y Y Year of release -i I IMDb movie id -r {JSON,XML} Return raw XML/JSON response --plot {short,full} Length of plot summary --tomatoes Include Rotten Tomatoes data too --type {movie,series,episode} movie, series, episode --season SEASON season number --episode EPISODE episode number --format {html,markdown,csv} Output formated in html, markdown or csv, leave out for text --apikey APIKEY Your API key (will try to use env var OMDB_API_KEY if omitted)

You can use any of these arguments and add to Dockerfile, it is based on how we want output.

Then execute the following command to build an Image.

 # docker build -t <reponame>:<tagname> .
Executing the program by running docker container to query a movie.

docker run -it
Movie :Pokiri                                                                                                              
IMDB Rating :7.9  
