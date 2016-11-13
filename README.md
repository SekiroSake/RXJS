# RXJS
RXJS
## Core Concepts
- Pull vs pull
  - Pull: normal model: uses external logic/controller to fetch model and apply views, in order to pull you have to repeatly fetch every certain period of time
  ```javascript
  windows.setInterval(() => {
   const tweets = ["x","y","z"]
      for (let tweet of tweets ){
        showTweet(){
        //...
        }
    },5000);
  ```
  - Push: observable model: the model itself knows when to change and show the view
  ```javascript
observeTweets()
  .subscribe(() => {
    showTweet()
  })
  ```
