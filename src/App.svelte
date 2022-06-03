<script>
  import HeroSection from "./lib/HeroSection.svelte";
  import SwitchTab from "./lib/SwitchTab.svelte";
</script>

<HeroSection />

<div class="locate-switch">

  <div class="component">
  <SwitchTab />
  </div>

  <div class="fake-component"/> 


</div>


<style>

  .locate-switch{
    display:flex;
    justify-content: space-around;
  }
  .component{
    width:600px;
  }

  .fake-component{
    width: 430px;
  }


</style>