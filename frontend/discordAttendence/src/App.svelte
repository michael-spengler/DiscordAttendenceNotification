<script>
  import Login from "@/components/Login.svelte";
  import Home from "@/components/Home.svelte";

  let page = "Login";
  let chatID = "abc";
  /*let writableStore = writable(chatID);

  setContext('ChatID', chatID);*/

  const controller = new AbortController();
  const signal = controller.signal;

  async function handleClickSubmitLoginParent() {
    const response = await fetch(
      `http://localhost:8800/api/v1/persistence/get/chatId/${chatID}`,
      { signal: signal, method: "GET" }
    );

    const exists = await response.text();

    if (exists === `true`) {
      page = "Home";
    }
  }
</script>

{#if page === "Login"}
  <Login bind:chatID />
{/if}

{#if page === "Home"}
  <Home bind:chatID />
{/if}

The chat ID is {chatID}

<style>
</style>
