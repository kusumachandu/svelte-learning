<script>

  let email = '';
  let password = '';

  let formValues = [];

  function submitHandler(e) {
    e.preventDefault();

    let formEmpty = {'email': email, 'password': password}

    formValues.push(formEmpty);

    email = '';
    password = '';

    alert(JSON.stringify(formEmpty));

    console.log(formValues)
  }
</script>

<div>
  <form id='form'>
    <label class="email">
      email
      <br />
      <input type="email" bind:value={email} />
    </label>
    <label class='password'>
      password
      <br />
      <input type="text" bind:value={password} />
    </label>
    <button type="submit" on:click={submitHandler}>Login</button>
  </form>
</div>

<style>
  div {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2px;
  }
  #form {
    display: flex;
    flex-direction: column;
    width: 100%;
    align-items: center;
    padding-bottom: 10%;
  }

  .email {
    width: 50%;
    display: flex;
    flex-direction: column;
    padding-top: 20px
  }

  .email input {
    width: 100%;
    padding: 10px;
    border: none;
    border-bottom: 2px solid gray;
    outline: none;
  }

  .password{
    width: 50%;
    padding-top: 20px;
    padding-bottom: 6%;
  }

  .password input {
    width: 100%;
    padding: 10px;
    border: none;
    border-bottom: 2px solid gray;
    outline: none;
  }

  button {
    padding: 10px;
    background-color: rgb(108, 108, 108);
    width: 30%;
    color: white;
    font-weight: 600;
    border-radius: 10px;
  }
</style>