# Testbook_Hackathon1_Survey-For-Project

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="Index.css">
    <title>Survey Form</title>
</head>

<body>
    <div class="container">
  <header class="header">
    <h1 id="title" class="text-center">Projects Survey Form</h1>
    <p id="description" class="description text-center">
      Thank you for taking the time to help us improve the platform
    </p>
  </header>
  <form id="survey-form">
    <div class="form-group">
      <label id="name-label" for="name">Name</label>
      <input type="text" name="name" id="name" class="form-control"placeholder="Enter your name" required/>
    </div>

    <div class="form-group">
      <label id="email-label" for="email">Email</label>
      <input type="email" name="email" id="email" class="form-control" placeholder="Enter your Email" required/>
    </div>

    <div class="form-group">
      <label id="number-label" for="number">Age</label>
      <input type="number" name="age" id="number" min="17" max="50" class="form-control" placeholder="Age"/>
    </div>
    <div class="form-group">
      <p>Which option best describes your current role?</p>
      <select id="dropdown" name="role" class="form-control" required>
        <option disabled selected value>Select current role</option>
        <option value="student">Student</option>
        <option value="job">Full Time Job</option>
        <option value="learner">Full Time Learner</option>
        <option value="preferNo">Prefer not to say</option>
        <option value="other">Other</option>
      </select>
    </div>

    <div class="form-group">
      <p>Would you recommend project </p>
      <label>
        <input name="user-recommend" value="definitely" type="radio" class="input-radio" checke/>Definitely</label>
      <label>
        <input name="user-recommend" value="maybe" type="radio" class="input-radio"/>Maybe</label>

      <label><input name="user-recommend" value="not-sure" type="radio" class="input-radio"/>Not sure</label>
    </div>

    <div class="form-group">
      <p>
        What is your favorite feature of freeCodeCamp?
      </p>
      <select> 
      <option value="Yes">Yes</option>
      <option value="NO">No</option>
    </select>
    </div>

    <div cInstragram
      <p>What would you next project</p>

      <label>
        <input  name="prefer"  value="Instragram"  type="checkbox"  class="input-checkbox"/>Instragram</label>
      <label>
        <input name="prefer" value="Twitter" type="checkbox" class="input-checkbox"/>Twitter</label>
      <label>
        <input name="prefer" value="Youtube" type="checkbox" class="input-checkbox"/>Youtube</label>
      <label>
        <input name="prefer" value="Any project Please Suggest me" type="checkbox" class="input-checkbox"/>Any project Please Suggest me</label>
      <label>
    </div>

    <div class="form-group">
      <p>Any comments or suggestions?</p>
      <textarea id="comments" class="input-textarea" name="comment" placeholder="Enter your comment here..."></textarea>
    </div>

    <div class="form-group">
      <button type="submit" id="submit" class="submit-button">Submit</button>
    </div>
  </form>
</div>
 
</body>
</html>

#CSS

@import url('https://fonts.googleapis.com/css?family=Poppins:200i,400&display=swap');

:root {
  --color-white: #f3f3f3;
  --color-darkblue: #1b1b32;
  --color-darkblue-alpha: rgba(27, 27, 50, 0.8);
  --color-green: #37af65;
}

*, *::before, *::after {
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.4;
  color: var(--color-white);
  margin: 0;
}

body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  z-index: -1;
  background: var(--color-darkblue);
  background-image: linear-gradient(
      115deg,
      rgba(58, 58, 158, 0.8),
      rgba(136, 136, 206, 0.7)
    ),
    url(https://cdn.freecodecamp.org/testable-projects-fcc/images/survey-form-background.jpeg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}

h1 {
  font-weight: 400;
  line-height: 1.2;
}

p {
  font-size: 1.125rem;
}

h1, p {
  margin-top: 0;
  margin-bottom: 0.5rem;
}

label {
  display: flex;
  align-items: center;
  font-size: 1.125rem;
  margin-bottom: 0.5rem;
}

input, button, select, textarea {
  margin: 0;
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}

button {
  border: none;
}

.container {
  width: 100%;
  margin: 3.125rem auto 0 auto;
}

@media (min-width: 576px) {
  .container {
    max-width: 540px;
  }
}

@media (min-width: 768px) {
  .container {
    max-width: 720px;
  }
}

.header {
  padding: 0 0.625rem;
  margin-bottom: 1.875rem;
}

.description {
  font-style: italic;
  font-weight: 200;
  text-shadow: 1px 1px 1px rgba(0, 0, 0, 0.4);
}

.clue {
  margin-left: 0.25rem;
  font-size: 0.9rem;
  color: #e4e4e4;
}

.text-center {
  text-align: center;
}


form {
  background: var(--color-darkblue-alpha);
  padding: 2.5rem 0.625rem;
  border-radius: 0.25rem;
}

@media (min-width: 480px) {
  form {
    padding: 2.5rem;
  }
}

.form-group {
  margin: 0 auto 1.25rem auto;
  padding: 0.25rem;
}

.form-control {
  display: block;
  width: 100%;
  height: 2.375rem;
  padding: 0.375rem 0.75rem;
  color: #495057;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ced4da;
  border-radius: 0.25rem;
  transition: border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}

.form-control:focus {
  border-color: #80bdff;
  outline: 0;
  box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);
}

.input-radio,
.input-checkbox {
  display: inline-block;
  margin-right: 0.625rem;
  min-height: 1.25rem;
  min-width: 1.25rem;
}

.input-textarea {
  min-height: 120px;
  width: 100%;
  padding: 0.625rem;
  resize: vertical;
}

.submit-button {
  display: block;
  width: 100%;
  padding: 0.75rem;
  background: var(--color-green);
  color: inherit;
  border-radius: 2px;
  cursor: pointer;
}
