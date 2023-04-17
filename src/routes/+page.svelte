<script>
import Header from "./Header.svelte";
import Footer from "./Footer.svelte";
  // API CODE......
</script>

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
