<script>
  export let chatID;

  // export let handleClickSubmitLogin = (chatID) => {};
  function handleClickSubmitLogin(chatID) {
    alert("user clicked login");
  }

  let listOfChatIDs = [];

  const controller = new AbortController();
  const signal = controller.signal;
</script>

<body class="bild">
  <h1><b>Please enter your Chat-ID: </b></h1>

  <div id="Login" class="user">
    <input id="chat_id" class="input" bind:value={chatID} />
    <button
      class="button"
      type="submit"
      onsubmit="return false"
      on:click={() => handleClickSubmitLogin()}>Submit</button
    >
  </div>

  <p>
    Contact our <a href="https://t.me/discordattendancenotificationbot"
      >Telegram-Bot</a
    > to get your Chat-ID.
  </p>
</body>

<style>
  h1 {
    color: white;
    font-size: 5em;
    font-weight: 200;
    margin-bottom: 4.5%;
  }

  p {
    color: white;
  }

  a {
    color: aqua;
  }

  .input {
    background-color: transparent;
    color: white;
    border: none;
    font-weight: 500;
    font-size: 17px !important;
    cursor: pointer;
    z-index: 1;
    padding: rem !important;
    font-size: 10px;
    box-shadow: 0 5px 12px -2px rgba(255, 255, 255, 0.3);
    text-align: center;
  }

  .button {
    background: rgba(255, 255, 255, 0.621);
    border: 1px solid rgba(255, 255, 255, 0.4);
    /*background-color: transparent;*/
    color: rgb(52, 17, 255);
    border: none;
    text-transform: uppercase;
    font-weight: 500;
    font-size: 17px !important;
    cursor: pointer;
    z-index: 1;
    padding: 1rem !important;
    font-size: 0.9rem !important;
    box-shadow: 0 5px 12px -2px rgba(0, 0, 0, 0.3);
  }
  .user {
    font-size: 1.1rem !important;
    padding: 0.6rem 1rem !important;
    position: relative;
    background: rgba(255, 255, 255, 0.185);
    border: 1px solid rgba(104, 12, 92, 0.4);
    border-bottom-color: rgba(168, 44, 158, 0.5);
    box-shadow: 0 5px 12px -2px rgba(0, 0, 0, 0.3);
    font-weight: 300;
    max-width: 20%;
    color: #cfd9e6;
    border-top-right-radius: 0;
    border-bottom-right-radius: 0;
    background-color: transparent;
    margin-left: 39%;
    border-radius: 150px;
    margin-bottom: 32%;
  }
  .user:hover {
    box-shadow: 0 10px 30px -2px rgba(0, 0, 0, 0.3);
    z-index: 0;
  }
  .user:focus {
    z-index: 0;
    background: rgba(0, 0, 0, 0.3);
    color: white;
  }
  .user:-webkit-input-placeholder {
    color: rgba(255, 255, 255, 0.4);
    font-size: 1.1rem;
  }
  .user:-moz-input-placeholder {
    color: rgba(255, 255, 255, 0.4);
    font-size: 1.1rem;
  }
  .user:-ms-input-placeholder {
    color: rgba(71, 94, 170, 0.4);
    font-size: 1.1rem;
  }
  .bild {
    background-image: url(https://th.bing.com/th/id/R.f05dac9a8d8f8b0fa0e81e8a46c54c91?rik=L74b%2fqnHB%2brLww&pid=ImgRaw&r=0);
    background-position: 30% 32%;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-size: cover;
  }
</style>
