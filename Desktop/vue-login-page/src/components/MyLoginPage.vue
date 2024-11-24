<template>
  <div class="login-interface">
    <div class="login-container">
      <div class="login-header">
        <h1>Barangay Name</h1>
        <h2>Municipality of Loreto <br> Province of Agusan del Sur</h2>
      </div>

      <div class="login-dropdown">
        <button @click="toggleDropdown" class="dropdown-btn">
          LOG IN AS
        </button>
        <ul v-if="dropdownVisible" class="dropdown-menu">
          <li>USER</li>
          <li>EMPLOYEE</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyLoginPage",
  data() {
    return {
      dropdownVisible: false,
    };
  },
  methods: {
    toggleDropdown() {
      this.dropdownVisible = !this.dropdownVisible;
    },
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}


/* Background style */
.login-interface {
  background: rgba(0, 36, 107, 1);
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0; 
  padding: 0; 
}

/* Container style */
.login-container {
  background:rgba(202, 220, 252, 0.6863);
  padding: 20px;
  border-radius: 30px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.25);
  width: 30%;
  height: 60%;
  text-align: center;
}

/* Header style */
.login-header h1 {
  font-size: 2.1rem;
  color: rgb(13, 13, 14);
margin-top: 5%;
padding-bottom: 10px;
}

.login-header h2 {
  font-size: 2.0rem;
  color: rgb(13, 13, 14);
  margin: 10px 0 20px;
}

/* Dropdown button */
.dropdown-btn {
  background-color:rgba(217, 217, 217, 1);
  color: rgb(0, 0, 0);
  font-size: 1.5rem;
  margin-top: 10%;
  padding: 10px 20px;
  text-align: left;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  width: 80%;
  height: 100%;
  
}

.dropdown-btn:hover {
  background-color: rgba(0, 36, 107, 0.9);
}

/* Dropdown menu */
.dropdown-menu {
  list-style-type: none;
  padding: 0;
  background:rgba(188, 188, 188, 1);
  border: 1px solid rgba(0, 36, 107, 0.3);
  border-radius: 1px;
  font-size: 1.5rem;
  text-align: left;
  margin-left: 10%;
  width: 80%;

}

.dropdown-menu li {
  padding: 10px;
  text-align: center;
  cursor: pointer;
  color:rgba(0, 0, 0, 0.45) ;
}

.dropdown-menu li:hover {
  background-color: rgba(0, 36, 107, 0.2);
}
/* Responsive Design */
@media (max-width: 768px) {
  .login-container {
    width: 80%;
    height: 40%;
    padding: 15px;

    border-radius: 20px;
  }

  .login-header h1 {
    font-size: 1.8rem;
  }

  .login-header h2 {
    font-size: 1.2rem;
  }

  .dropdown-btn {
    font-size: 1.2rem;
    padding: 10px;
  }

  .dropdown-menu {
    font-size: 1.2rem;
  }
}

@media (max-width: 480px) {
  .login-header h1 {
    font-size: 1.5rem;
  }

  .login-header h2 {
    font-size: 1rem;
  }

  .dropdown-btn {
    font-size: 1rem;
    padding: 8px;
  }

  .dropdown-menu {
    font-size: 1rem;
  }
}
</style>