<script lang="ts">
  /**
    * index.svelte is where we are rendering our site. 
    * Header.svelte is the header/navigation component.
    * Landing.svelte is our landing page with our sveltable logo and description.
    * Features.svelte is our text description of features within Sveltable.
    * Demo.svelte is a component containing a gif of creating a table component and a description of it.
  */ 

  import Header from '../lib/Header.svelte';
  import Landing from '../lib/Landing.svelte';
  import Features from '../lib/Features.svelte';
  import Demo from '../lib/Demo.svelte';
</script>

<!-- Loading app -->
<div class="AppContainer">
  <!-- Navigation Header -->
  <div class="HeaderContainer">
    <Header />
  </div>
  <!-- Landing body -->
  <div class="LandingContainer">
    <Landing />
  </div>
  <!-- Demo section -->
  <div class="DemoContainer">
    <!-- <Demo /> -->
  </div>
  <!-- Features section -->
  <div class="FeatureContainer">
    <Features />
  </div>
</div>

<style>
  .AppContainer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .LandingContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
  }

  .DemoContainer {
    min-height: 100vh;
  }

  .FeatureContainer {
    min-height: 100vh;
  }
</style>
