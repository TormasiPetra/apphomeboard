<script lang="ts">
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import Header from "./Components/Header.svelte";
  import Footer from "./Components/Footer.svelte";
  import NotFound from "./routes/Notfound.svelte";
  import Terms from "./routes/Terms.svelte";
  import Privacy from "./routes/Privacy.svelte";
  import { fade } from "svelte/transition";

  export let url = "";
</script>

<Router {url}>
  <Header />
  <div class="">
    <Route path="/"><Home /></Route>
    <Route path="/privacy"><Privacy /></Route>
    <Route path="/terms"><Terms /></Route>
  </div>
  <Footer />
</Router>
