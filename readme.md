## Firebase

### in container
```
docker run -it --rm -p 8800:8800 -p 8080:8080 -p 4400:4400 -p 9005:9005 -v $(pwd):/tmp/filebase ubuntu:24.04 /bin/bash

docker run -it --rm -p 4200:4200 -v $(pwd):/tmp/org node:20 /bin/bash
```

### install firebase-tools

```
apt update
apt install -y nodejs node-gyp npm
sudo npm install -g firebase-tools
npm add --global nx@latest
firebase help
```

### filebase init

```
firebase login

firebase apphosting:backends:create --project PROJECT_ID --location us-central1
# example
firebase apphosting:backends:create --project liduan-blog --location us-central1

firebase apphosting:backends:delete --project liduan-blog firebase-auth-page


```


## app hosting

### init
```
npm init @apphosting
```



git remote add origin git@github.com:duan-li/apphosting-example.git


# Next.js on Firebase App Hosting (generate by `npm init @apphosting`)

This is an example [Next.js](https://nextjs.org/) project to demonstrate SSG,
SSR, and ISR on [Firebase App Hosting](https://firebase.google.com/docs/app-hosting).

## Getting Started

Run the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Deploy to Firebase App Hosting

### 1. Get your project set up on GitHub

[Create a new GitHub repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository) and push the newly-initialized sample code to it:

<pre>
git remote add origin https://github.com/<b>$YOUR_NEW_REPOSITORY</b>.git
git branch -M main
git push -u origin main
</pre>

### 2. Set up Firebase App Hosting

Continue to [Get started with Firebase App Hosting](https://firebase.google.com/docs/app-hosting/get-started#step-1:).
