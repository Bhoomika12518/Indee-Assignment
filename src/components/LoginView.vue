<template>
  <div class="overlay"></div>
  <div id="app" class="">
    <div
      class="card black-theme text-white mb-3 centered-card"
      style="width: 20rem"
    >
      <div class="card-body">
        <div class="card-title text-center">
          <h5>
            <span style="font-size: 2rem">MGM</span>
            Global Distribution
          </h5>
        </div>
        <h5 class="py-2">Sign in</h5>
        <form @submit.prevent="login">
          <div class="form-group">
            <label for="email" class="blue-label">Email</label>
            <input
              type="email"
              class="form-control grey-input"
              id="email"
              v-model="email"
              required
              placeholder="Enter your email address"
            />
          </div>
          <div class="form-group">
            <label for="password" class="blue-label">Password</label>
            <input
              type="password"
              class="form-control grey-input"
              id="password"
              v-model="password"
              required
              placeholder="Enter your password"
            />
          </div>
          <div class="form-group text-right">
            <a href="#" class="forgot-password">Forgot Password?</a>
          </div>
          <div class="form-check py-2">
            <input type="checkbox" class="form-check-input" id="keepSignedIn" />
            <label class="form-check-label forgot-password" for="keepSignedIn"
              >Keep me signed in for 30 days</label
            >
          </div>
          <button type="submit" class="btn btn-primary btn-block">
            Sign in
          </button>
          <div class="form-group mt-2">
            <a href="#" class="text-muted">
              <i class="fas fa-book"></i>
              Read our Terms of service
            </a>
          </div>
        </form>
      </div>
      <div class="card-footer">
        <img src="../assets/footer.png" alt="Logo" style="max-width: 275px" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LoginView",
  data() {
    return {
      email: "",
      password: "",
    };
  },
  methods: {
    login() {
      console.log("Email:", this.email);
      console.log("Password:", this.password);
      if (
        this.email === "test@gmail.com" &&
        this.password === "password"
      ) {
        alert("Login Successfull!");
      } else {
        // For demonstration, show an alert for unsuccessful login
        alert("Invalid email or password.");
      }
    },
  },
};
</script>

<style>
.centered-card {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.black-theme {
  background-color: #000000;
  color: #ffffff;
}

.blue-label {
  color: rgb(48, 48, 239);
}

.grey-input {
  background-color: rgb(59, 58, 58);
}

.forgot-password {
  color: grey;
}

.card-title {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.card-title h5 {
  font-size: 1.5rem;
}

body {
  background-image: url("https://cdn.mos.cms.futurecdn.net/rDJegQJaCyGaYysj2g5XWY-1200-80.jpg");
  background-size: cover;
  background-position: center;
  height: 100vh;
  margin: 0;
  padding: 0;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.75);
}
</style>
