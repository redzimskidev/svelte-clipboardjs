<script>
  let message = 'Nothing copied yet.';
  const bc = new BroadcastChannel('clipboard');
  bc.onmessage = (event) => {
    if (event.data.success) {
      message = 'Succesfully copied at ' + new Date().toLocaleTimeString();
    } else {
      message = 'Failed to copy at ' + new Date().toLocaleTimeString();
    }
  };
</script>

<div id="container">
  <h1>Look at those awesome pictures!</h1>
  <img src="https://picsum.photos/200/200" alt="Random" />
  <img src="https://picsum.photos/250/200" alt="Random" />
  <img src="https://picsum.photos/150/200" alt="Random" />
</div>

<button class="btn" data-clipboard-target="#container">Copy</button>
<p>{message}</p>
