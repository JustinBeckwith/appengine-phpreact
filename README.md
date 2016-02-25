# PHP React -> Google App Engine

This is a simple guide to running phpreact on Google App Engine. 

1. [Create a new PHP React app](http://reactphp.org/)

2. Create an `app.yaml` in the root of your application with the following contents:

    ```yaml
    runtime: custom
    vm: true
    ```

3. Create a `Dockerfile` in the root of your application with the following contents:

    ```dockerfile
    FROM gcr.io/php-mvm-a/php-nginx:latest
    ```
4. Create a project in the [Google Developers Console](https://console.developers.google.com/).

5. Make sure you have the [Google Cloud SDK](https://cloud.google.com/sdk/) installed. 

    ```sh
    $ curl https://sdk.cloud.google.com | bash 
    $ gcloud init
    $ gcloud components update app
    ```

6. Deploy your app:

    ```sh
    gcloud preview app deploy
    ```

You are now running PHP React on App Engine. How cool is that?  Check it out at [https://phpreact-demo.appspot.com/](https://phpreact-demo.appspot.com/).
