<script>
import Header from "./Header.svelte";
import Footer from "./Footer.svelte";
  import { onMount } from "svelte";

  onMount(async () => {
    // Code goes here
  });
</script>

<svelte:head>
  <script
    type="text/javascript"
    src="https://cdn.jsdelivr.net/npm/@voxeet/voxeet-web-sdk/dist/voxeet-sdk.js"
  ></script>
  <script
    type="text/javascript"
    src="https://developer.dolby.io/demos/comms-sdk-web-getting-started/util/dolbyio-auth-helper.js"
  ></script>

  <script
    src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p"
    crossorigin="anonymous"
  ></script>
</svelte:head>

<Header />

<div class="video_container">
  <div class="video_wrapper">
    <div id="self-view">
      <!-- Container for the local participant media stream -->
      <p id="self-view-username" />
      <i class="display-1 bi bi-person-video position-relative" />
    </div>
  </div>

  <div class="video_wrapper">
    <div id="remote-view">
      <!-- Container for the remote participant media stream -->
      <p id="remote-view-username" />
      <i class="display-1 bi bi-person-video position-relative" />
    </div>
  </div>
</div>

<br />


<Footer />


<style>

  .video_container {
    width: 80%;
    height: 60vh;
    margin: auto;
    display: flex;
    padding: 10px;
    justify-content: space-between;
  }

  @media (max-width: 600px) {
    .video_container {
      flex-direction: column;
      width: 100%;
    }
  }

  .video_wrapper {
    flex-basis: 45%;
    background-color: rgb(43 47 49);
    border: 10px;
    height: 100%;
    border-radius: 10px;
  }

  


</style>
