<script>


export default {
  data() {
    return {
      searchInput: "",
    };
  },
  methods: {
    search() {
      const input = this.searchInput;
      console.log("hello world");
      window.location.href = "https://www.google.com/search?q="
        + input +
        "&lz=1C5CHFA_enNZ948NZ948&oq="
        + input +
        "&aqs=chrome.0.69i59l2j46i175i199i433j46i199i291i433j46j0i433j0j69i60.875j0j9&sourceid=chrome&ie=UTF-8";
    },
  },
};
</script>

<template>
  <body>
<header>
  <nav class="navbar">
    <ul>
      <li>
        <a class="link" href="https://mail.google.com/mail/u/0/?tab=wm#inbox">Gmail</a>
      </li>
      <li>
        <a class="link" href="https://www.google.com.et/imghp?hl=en&ogbl">Images</a>
      </li>
      <li>
        <div class="circle-shadow">
          <a class="menu-icon" href=""><i class="fas fa-bars"></i></a>
        </div>
      </li>
      <li>
        <div class="circle-shadow">
          <a class="user-icon" href=""><span>J</span></a>
        </div>
      </li>
    </ul>
  </nav>
</header>

<!-- Content -->
<section class="content-section">
  <div class="content-wrapper">
    <img class="logo-img" src="./assets/logo.jpg" alt="Google Logo Image">
    <div class="search-bar">
      
      <i class="fas fa-search" @click="search"></i>
      <input id="search-input" class="search-input" type="text" v-model="searchInput" @keydown.enter="search">
      <i class="fas fa-keyboard"></i>
      <i class="fas fa-microphone"></i>
    </div>
    <div class="search-btns">
      <button class="google-search-btn" @click="search">Google Search</button>
      <button class="lucky-search-btn"><a href="https://www.google.com/doodles">I'm Feeling Lucky</a></button>
    </div>
    <div class="language">
      <p>Google clone made by: <a href="https://github.com/YOSEF-CODER">Yosef Lakew</a></p>
    </div>
  </div>
</section>

<!-- Footer -->
<footer>
  <div class="footer-content upper-footer">
    <p>Ethiopia</p>
  </div>
  <div class="footer-content lower-footer">
    <ul class="lower-left-footer">
      <li>
        <a href="https://about.google/?utm_source=google-NL&utm_medium=referral&utm_campaign=hp-footer&fg=1">About</a>
      </li>
      <li>
        <a href="https://ads.google.com/intl/en_nl/home/?subid=ww-ww-et-g-awa-a-g_hpafoot1_1!o2&utm_source=google.com&utm_medium=referral&utm_campaign=google_hpafooter&fg=1">Advertising</a>
      </li>
      <li>
        <a href="https://www.google.com/services/?subid=ww-ww-et-g-awa-a-g_hpbfoot1_1!o2&utm_source=google.com&utm_medium=referral&utm_campaign=google_hpbfooter&fg=1#?modal_active=none">Business</a>
      </li>
      <li>
        <a href="https://www.google.com/search/howsearchworks/?fg=1">How Search Works</a>
      </li>
    </ul>
    <ul class="lower-right-footer">
      <li>
        <a href="https://policies.google.com/privacy?hl=en-NL&fg=1">Privacy</a>
      </li>
      <li>
        <a href="https://policies.google.com/terms?hl=en-NL&fg=1">Terms</a>
      </li>
      <li>
        <a href="">Settings</a>
      </li>
    </ul>
  </div>
</footer>
  </body>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

li {
  list-style-type: none;
}

a {
  text-decoration: none;
}

body {
  font-family: sans-serif;
  height: 100vh;
  display: flex;
  flex-direction: column;
}

/* Header */
header {
  height: 60px;
}

.navbar {
  height: 100%;
  width: 100%;
  padding: 30px 20px;
}

.navbar ul {
  height: 100%;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  font-size: 14px;
}

.navbar ul li {
  margin-left: 15px;
}

.navbar ul li a {
  color: black;
 
}

.link:hover {
  text-decoration: underline;
}

.circle-shadow {
  height: 40px;
  width: 40px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.circle-shadow:hover {
  background-color: rgba(0, 0, 0, 0.1);
}

.menu-icon,
.user-icon span {
  font-size: 18px;
}

.user-icon span {
  color: white;
}

.user-icon {
  background-color: #EF6C00;
  height: 30px;
  width: 30px;
  border-radius: 50%;
  text-align: center;
  line-height: 30px;
}

/* Content */
.content-section {
  flex-grow: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.content-wrapper {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-bottom: 100px;
}

.logo-img {
  width: 300px;
  margin-bottom: 20px;
}

.search-bar {
  border: 1px solid lightgray;
  width: 600px;
  height: 45px;
  border-radius: 30px;
  display: flex;
  align-items: center;
  padding-left: 15px;
}

.search-bar:hover {
  box-shadow: 0px 0px 4px 0px #B5B5B5;
}

.search-bar i {
  font-size: 18px;
  color: gray;
  margin-right: 15px;
  cursor: pointer;
}

.search-bar input {
  flex-grow: 1;
  height: 30px;
  margin-right: 15px;
  font-size: 16px;
  border: none;
}

.search-bar input:focus {
  outline: none;
}

.search-btns {
  margin-top: 20px;
}

.search-btns button {
  height: 40px;
  font-size: 14px;
  border: none;
  border-radius: 5px;
  margin-left: 10px;
  color: black;
  background-color: #F2F3F4;
}

.search-btns button:hover {
  border: 1px solid lightgray;
}

.google-search-btn {
  width: 120px;
}

.lucky-search-btn {
  width: 140px;
}

.language {
  margin-top: 20px;
  font-size: 14px;
}

.language p a {
  color: blue;
}

.language p a:hover {
  text-decoration: underline;
}

/* Footer */
footer {
  background-color: #F2F2F2;
  height: 100px;
}

.footer-content {
  display: flex;
  align-items: center;
  padding: 20px;
}

.upper-footer {
  height: 50%;
  border-bottom: 1px solid lightgray;
}

.upper-footer p {
  color: gray;
  font-size: 14px;
}

.lower-footer {
  height: 50%;
  display: flex;
  justify-content: space-between;
}

.lower-footer ul li a {
  font-size: 14px;
  color: gray;
}

.lower-footer ul li a:hover {
  text-decoration: underline;
}

.lower-left-footer {
  display: flex;
}

.lower-left-footer li {
  margin-right: 15px;
}


.lower-right-footer {
  display: flex;
}

.lower-right-footer li {
  margin-left: 15px;
}

/* Mobile and Tablet */
@media only screen and (max-width: 650px) {

  /* Navbar */
  .navbar ul {
    font-size: 10px;
  }

  .menu-icon,
  .user-icon span {
    font-size: 14px;
  }

  .circle-shadow {
    height: 30px;
    width: 30px;
  }

  /* Logo */
  .logo-img {
    width: 200px;
  }

  /* Search Bar */
  .search-bar {
    width: 90%;
    height: 35px;
  }

  .search-bar i {
    font-size: 14px;
  }

  /* Buttons */
  .search-btns button {
    height: 30px;
    font-size: 12px;
  }

  .google-search-btn {
    width: 100px;
  }

  .lucky-search-btn {
    width: 120px;
  }

  /* Language */
  .language {
    font-size: 12px;
  }

  /* Footer */
  footer {
    height: 150px;
  }

  .upper-footer {
    height: 50px;
  }

  .lower-footer {
    height: 100px;
    flex-direction: column;
  }

  .lower-left-footer {
    flex-wrap: wrap;
  }
}
</style>
