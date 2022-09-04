<script>
  import {Route} from 'tinro'; 

  import Full from '../src/lib/full.svelte';
  import Beta from '../src/lib/beta.svelte';
</script>

<main>
  <Route path="/">
    <Full />
	</Route>
	
	<Route path="/beta">
		<Beta />
	</Route>
</main>
