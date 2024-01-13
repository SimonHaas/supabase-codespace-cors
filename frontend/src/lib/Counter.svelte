<script>
  let count = 0;
  const increment = () => {
    count += 1;
  };

  fetch(`${import.meta.env.VITE_SUPABASE_URL}/functions/v1/hello-world`, {
    headers: {
      "X-Github-Token": import.meta.env.VITE_GITHUB_TOKEN,
    },
  });
</script>

<button on:click={increment}>
  count is {count}
</button>
