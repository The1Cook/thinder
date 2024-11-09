<!-- src/Login.svelte -->
<script>
    let username = '';
    let password = '';
    let errorMessage = '';
    let isLoading = false;
  
    // Simple validation and login handler (you can replace with actual logic)
    const handleLogin = () => {
      // Clear any previous error message
      errorMessage = '';
  
      if (!username || !password) {
        errorMessage = 'Username and password are required.';
        return;
      }
  
      // Simulate an API call (replace with actual logic)
      isLoading = true;
      setTimeout(() => {
        if (username === 'user' && password === 'password') {
          alert('Login successful!');
          // Redirect or set some state for logged-in user here
        } else {
          errorMessage = 'Invalid username or password.';
        }
        isLoading = false;
      }, 1000);
    };
  </script>
  
  <style>
    .login-container {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #f4f4f9;
    }
  
    .login-box {
      background: white;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      width: 300px;
    }
  
    .login-box h2 {
      text-align: center;
      margin-bottom: 20px;
    }
  
    .input-group {
      margin-bottom: 15px;
    }
  
    .input-group label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
    }
  
    .input-group input {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 1em;
    }
  
    .input-group input:focus {
      border-color: #007bff;
      outline: none;
    }
  
    .error-message {
      color: red;
      font-size: 0.9em;
      margin-bottom: 10px;
    }
  
    .submit-button {
      width: 100%;
      padding: 10px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 1.1em;
    }
  
    .submit-button:disabled {
      background-color: #ccc;
      cursor: not-allowed;
    }
  
    .submit-button:focus {
      outline: none;
    }
  
    .loading-spinner {
      display: inline-block;
      border: 3px solid #f3f3f3;
      border-top: 3px solid #007bff;
      border-radius: 50%;
      width: 24px;
      height: 24px;
      animation: spin 1s linear infinite;
    }
  
    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
  </style>
  
  <div class="login-container">
    <div class="login-box">
      <h2>Login</h2>
      {#if errorMessage}
        <div class="error-message">{errorMessage}</div>
      {/if}
      <div class="input-group">
        <label for="username">Username</label>
        <input
          id="username"
          type="text"
          bind:value={username}
          placeholder="Enter username"
          autofocus
        />
      </div>
      <div class="input-group">
        <label for="password">Password</label>
        <input
          id="password"
          type="password"
          bind:value={password}
          placeholder="Enter password"
        />
      </div>
      <button
        class="submit-button"
        on:click={handleLogin}
        disabled={isLoading}
      >
        {#if isLoading}
          <div class="loading-spinner"></div> Loading...
        {:else}
          Login
        {/if}
      </button>
    </div>
  </div>
  