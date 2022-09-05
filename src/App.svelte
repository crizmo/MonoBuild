<script>
  import {Route} from 'tinro'; 

  import Full from './routes/full.svelte';
  import Beta from './routes/beta.svelte';
</script>

<main>
  <Route path="/">
    <Full />
	</Route>
	
	<Route path="/beta">
		<Beta />
	</Route>
</main>
