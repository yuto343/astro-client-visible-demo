<script>
  import { onMount } from "svelte";

  let count = 0;

  function countUp() {
    count += 1;
  }

  onMount(() => {
    const interval = setInterval(countUp, 1000);

    return () => {
      clearInterval(interval);
    };
  });
</script>

<div>
  Count：{count}
</div>

<style>
  div {
    font-size: 30px;
    font-weight: bold;
  }
</style>
