<script>
    import fblogo from "$lib/images/social/facebook-blue.svg";
</script>



    <div class="regform">
      <h1>Create your Account</h1>
      <div class="regdiv">
        <h3>User Information</h3>
        <div class="Textbox">
          <input
            class="input"
            placeholder="First name"
            type="text"
            required
            id="fname"
          />
          <input
            class="input"
            placeholder="Last name"
            type="text"
            required
            id="lname"
          />
        </div>
        <div class="gendiv">
          <h3>Gender</h3>
          <input
            class="radio"
            type="radio"
            name="gender"
            id="Male"
            value="Male"
          />
          <label>ㅤMaleㅤㅤ</label>
          <input
            class="radio"
            type="radio"
            name="gender"
            id="Female"
            value="Female"
          />
          <label>ㅤFemale</label>
          <h3>ㅤㅤㅤㅤㅤㅤㅤㅤㅤ</h3>
          <h3>Date of Birth:</h3>
          <input type="date" class="birth" id="bday" />
        </div>
        <div>
          <h3>Login & Credentials</h3>
          <input
            class="input"
            placeholder="E-mail"
            type="text"
            required
            id="email"
          />
          <input
            class="input"
            placeholder="Phone Number"
            type="text"
            required
            id="phonenum"
          />
          <input
            class="input"
            placeholder="Password"
            type="password"
            required
            id="password"
          />
          <input
            class="input"
            placeholder="Confirm Password"
            type="password"
            required
            id="confirm_password"
          />
        </div>
        <div class="divstyle">
          <h4>
            ㅤBy clicking Create your account below,<br />
            ㅤㅤyou've read the full text and agreed<br />
            to the <a href="/register">Terms & Conditions</a> and
            <a href="/register">Privacy Policy.</a>
          </h4>
        </div>

        <input
          type="button"
          value="Create your Account"
          class="regBtn"
          id="RegBtn"
        />
        <br />

        <div class="divline">
          <h5>__________________________________________________________</h5>
          <h5>ㅤㅤ</h5>
          <h3>OR</h3>
          <h5>ㅤㅤ</h5>
          <h5>_________________________________________________________</h5>
        </div>
        <button class="signup-with-facebook">
          <img src={fblogo} alt="facebook logo" />
          <p>Sign up with Facebook</p>
        </button>
        <div class="divstyle">
          <h4>Already have an account? <a href="signin.html">Log in</a></h4>
        </div>
      </div>
    </div>


  <style>
    * {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.bg {
  background-image: url(/../assets/bg_homepage.png);
  background-size: 100%;
  min-height: 100%;
  font-family: Arial, Helvetica, sans-serif;
}
.regform {
  display: flex;
  align-items: center;
  position: relative;
  flex-direction: column;
  max-width: fit-content;
  position: relative;
  left: 50%;
  height: 100%;
  padding-top: 50px;
  padding-bottom: 40px;
  transform: translateX(-50%);
  color: white;
}

.regform h1 {
  font-size: 28px;
  word-spacing: 1px;
}

.regdiv {
  display: flex;
  position: relative;
  align-items: left;
  border: 2px solid white;
  border-radius: 20px;
  flex-direction: column;
  width: 1000px;
  position: relative;
  left: 50%;
  height: fit-content;
  padding-top: 20px;
  padding-bottom: 10px;
  padding-left: 20px;
  transform: translateX(-50%);
  color: white;
}
.columndiv {
  display: flex;
  flex-direction: column;
  max-width: fit-content;
  position: relative;
}

.Btncontainer {
  align-self: center;
  align-content: center;
}
.regBtn {
  align-self: center;
  background-color: transparent;
  border-radius: 28px;
  border: 1px solid #ffffff;
  display: inline-block;
  cursor: pointer;
  color: #ffffff;
  font-family: Arial;
  font-size: 15px;
  padding: 10px 22px;
  text-decoration: none;
  text-shadow: 0px 1px 0px #2f6627;
  font-weight: bold;
  width: 300px;
}
.regBtn:hover {
  background-color: #cbafe7;
  color: #371d50;
}

.regBtn:active {
  position: relative;
  top: 2px;
}

.Textbox {
  display: flex;
  flex-direction: row;
  align-items: center;
  position: relative;
  max-width: 100%;
  margin: 10px;
  padding-left: 10px;
}
.input {
  font-size: 13px;
  padding: 10px 20px;
  width: 100%;
  outline: none;
  background: #d3b5f0;
  color: #000000;
  border: 1px solid #62457c;
  border-radius: 100px;
  transition: 0.3s ease;
  margin: 5px;
  width: 450px;
  opacity: 0.65;
}
.radio {
  font-size: 13px;
  padding: 10px 20px;
  width: 100%;
  outline: none;
  background: #d3b5f0;
  color: #000000;
  border: 1px solid #62457c;
  border-radius: 100px;
  transition: 0.3s ease;
  margin-left: 15px;
  width: fit-content;
  opacity: 0.65;
}

.input:focus {
  background: #cbafe7;
  border: 1px solid #62457c;
  border-radius: 10px;
}

.input::placeholder {
  color: black;
}

.divstyle {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 25px;
  margin-bottom: 20px;
}
.divstyle h4 {
  font-size: 12px;
  font-weight: normal;
}

.divstyle a {
  color: #cbafe7;
}
.divstyle a:hover {
  color: #371d50;
}
.divline {
  margin-left: 20px;
  margin-right: 20px;
  display: flex;
  flex-direction: row;
}

.signup-with-facebook {
  display: flex;
  flex-direction: row;
  position: relative;
  gap: 10px;
  justify-content: center;
  max-width: 300px;
  cursor: pointer;
  flex-wrap: nowrap;
  border-radius: 20px;
  border: solid;
  border-width: 1px;
  color: white;
  border-color: white;
  left: 50%;
  transform: translateX(-50%);
  box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px,
    rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
  padding: 10px;
  background-color: transparent;
  margin-top: 20px;
  margin-bottom: -10px;
}
.signup-with-facebook:hover {
  background-color: #cbafe7;
  color: #000000;
}

.signup-with-facebook:active {
  position: relative;
  top: 2px;
}
.birth::-webkit-calendar-picker-indicator {
  background: transparent;
  bottom: 0;
  color: transparent;
  cursor: pointer;
  height: auto;
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  width: auto;
}
.birth {
  background-color: #62457c;
  margin-left: 10px;
  color: #ffffff;
  width: 200px;
  padding-left: 55px;
  justify-content: space-evenly;
}

.gendiv {
  margin-left: 20px;
  margin-right: 20px;
  display: flex;
  flex-direction: row;
  margin-bottom: 20px;
  margin-top: 20px;
}

  </style>