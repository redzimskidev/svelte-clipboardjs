<script>
  import Clipboard from 'clipboard';
  import { onMount } from 'svelte';
  let message = 'Nothing copied yet.';

  onMount(() => {
    let clipboard = new Clipboard('.btn');
  });
</script>

<div id="container">
  <h1>Look at those awesome pictures!</h1>
  <img src="https://picsum.photos/200/200" alt="Random" />
  <img src="https://picsum.photos/250/200" alt="Random" />
  <img src="https://picsum.photos/150/200" alt="Random" />
</div>

<button class="btn" data-clipboard-target="#container">Copy</button>
<p>{message}</p>
