<script>
  import { Router, Route } from 'yrv';

  import Index from './pages/Index.svelte';
  import Climbers from './pages/Climbers.svelte';
  import Routes from './pages/Routes.svelte';
  import Mission from './pages/Mission.svelte';
</script>

<Router>
  <Route exact component={Index} />
  <Route fallback>Not found</Route>
  <Route exact path="#climbers" component={Climbers}/>
  <Route exact path="#routes" component={Routes}/>
  <Route exact path="#mission" component={Mission}/>
</Router>