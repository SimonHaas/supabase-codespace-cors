<script lang="ts">
  fetch(`${import.meta.env.VITE_SUPABASE_URL}/functions/v1/hello-world`, {
    headers: {
      "X-Github-Token": import.meta.env.VITE_GITHUB_TOKEN,
    },
  });
</script>
