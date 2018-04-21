## About

This is a quick [demo](https://davidwu220.github.io/dog-breed-masonry/) which lazy-loads all images from the [Dog API](https://dog.ceo/dog-api/).

This app is bootstrapped using `create-react-app` with following packages installed:

* [axios](https://github.com/axios/axios) for http get requests.
* [material-ui](https://github.com/mui-org/material-ui) for making the card component looks nicer.
* [react-virtualized](https://github.com/bvaughn/react-virtualized) for just-in-time component rendering and for masonry support.

---

## TODO

There are some improvments I'd like to make if given more time.

* **Implement dynamic heights** so the image ratio is closer to original as shown in example [here](https://codesandbox.io/s/xj807vkjpq).  
  Note that the solution implemented in the example requires heavy overhead computing. If the image list is large (20k+, take the dog-api for example), the performance will drop significantly.  
  One way to improve this is to set up a server that computes the image dimensions before serving them to client side.
* **Animation**: I've tried many different animation libraries but they don't work well (or straight up didn't work) with `react-virtualized`. [Here](https://codesandbox.io/s/w6w7j7y0j7) is an example that I implemented with [react-transition-group](https://github.com/reactjs/react-transition-group). Notice the flickering of the images which makes this solution not ideal.
* **Improve styling for mobile view**: currently the responsive window size only supports `width`s down to `400px`.