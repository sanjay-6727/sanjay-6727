<h1 align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=28&duration=3000&pause=800&color=00FF99&center=true&vCenter=true&width=600&lines=hey+im+sanjay;CSE+student;Full+Stack+Developer;"/>
</h1>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=sanjay-6727&label=Visitors&color=00ff99&style=flat" />
</p>

---

<p align="center">
  <img src="https://raw.githubusercontent.com/sanjay-6727/sanjay-6727/main/dist/snake.svg" />
</p>

---


## SYSTEM ACTIVITY

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=sanjay-6727&show_icons=true&theme=vision-friendly-dark&hide_border=true&title_color=00ff99&icon_color=00ff99&text_color=ffffff" height="165"/>

<img src="https://streak-stats.demolab.com?user=sanjay-6727&theme=vision-friendly-dark&hide_border=true&ring=00ff99&fire=00ff99&currStreakLabel=00ff99" height="165"/>

</div>

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=sanjay-6727&theme=react-dark&bg_color=0d1117&color=00ff99&line=00ff99&point=ffffff&hide_border=true"/>

</div>

---

## TECH STACK

### Core Languages
<p align="center">
  <img src="https://skillicons.dev/icons?i=cpp,java,python,c,js,ts&theme=dark" />
</p>

###  Web Stack
<p align="center">
  <img src="https://skillicons.dev/icons?i=html,css,react,nextjs,nodejs,express,tailwind&theme=dark" />
</p>

### Mobile Systems
<p align="center">
  <img src="https://skillicons.dev/icons?i=flutter,dart&theme=dark" />
</p>

### Data & Infrastructure
<p align="center">
  <img src="https://skillicons.dev/icons?i=oracle,mysql,postgres,firebase,docker,linux,vercel&theme=dark" />
</p>

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=0:00ff99,100:000000&height=2"/>
</p>

<p align="center">
  <code style="color:#00ff99;">
  > i write code.<br/>
  > sometimes the code writes back.<br/>
  > we maintain an understanding.
  </code>
</p>

/*
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ATM Machine</title>
  <style>
    body{
      background:linear-gradient(135deg,#000000,rgb(155,0,0),#f79800);
      font-family:Poppins,sans-serif;
      color:white;
      margin:0;
      min-height:100vh;
    }

    .navbar{
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:15px 30px;
      background:linear-gradient(135deg,#000000,rgb(155,0,0),#f79800);
      box-shadow:0 4px 10px rgba(0,0,0,0.4);
    }

    .logo{
      font-size:24px;
      font-weight:bold;
    }

    .nav-links{
      list-style:none;
      display:flex;
      gap:25px;
      padding:0;
      margin:0;
    }

    .nav-links li a{
      color:white;
      text-decoration:none;
      font-weight:bold;
      cursor:pointer;
    }

    .container{
      display:flex;
      flex-direction:column;
      justify-content:center;
      align-items:center;
      padding:40px 20px;
    }

    .card{
      background:rgba(255,255,255,0.1);
      backdrop-filter:blur(10px);
      padding:30px;
      border-radius:20px;
      width:90%;
      max-width:500px;
      box-shadow:0 8px 20px rgba(0,0,0,0.4);
      margin-top:20px;
    }

    h1,h2{
      text-align:center;
    }

    .form-group{
      display:flex;
      flex-direction:column;
      gap:15px;
      margin:20px 0;
    }

    input{
      padding:12px;
      border:none;
      border-radius:10px;
      font-size:16px;
    }

    button{
      padding:12px;
      border:none;
      border-radius:10px;
      background:#ff9800;
      color:white;
      font-size:16px;
      font-weight:bold;
      cursor:pointer;
      transition:0.3s;
    }

    button:hover{
      background:#ff6f00;
      transform:scale(1.03);
    }

    #dashboard{
      display:none;
    }

    #output{
      font-size:18px;
      text-align:center;
      margin-bottom:20px;
      line-height:1.8;
    }
  </style>
</head>
<body>

  <nav class="navbar">
    <div class="logo">ATM MACHINE</div>
    <ul class="nav-links">
      <li><a onclick="showSection('login')">LOGIN</a></li>
      <li><a onclick="showSection('dashboard')">DASHBOARD</a></li>
    </ul>
  </nav>

  <div class="container">

    <div class="card" id="loginSection">
      <h1>LOGIN TO YOUR BANK ACCOUNT</h1>
      <div class="form-group">
        <input id="accountnumber" placeholder="Enter account no">
        <input id="pswd" type="password" placeholder="Enter Password">
        <button onclick="login()">LOG IN</button>
      </div>
    </div>

    <div class="card" id="dashboard">
      <h1>ATM Dashboard</h1>
      <p id="output"></p>

      <h2>Deposit</h2>
      <div class="form-group">
        <input type="number" placeholder="Enter amount to deposit" id="dep">
        <button onclick="deposit()">Submit</button>
      </div>

      <h2>Withdraw</h2>
      <div class="form-group">
        <input type="number" placeholder="Enter amount to withdraw" id="wid">
        <button onclick="withdraw()">Submit</button>
      </div>
    </div>

  </div>

  <script>
    let users=[
      {account:"123",p:"123",balance:4000},
      {account:"12",p:"12",balance:7000}
    ];

    function showSection(section){
      if(section==='login'){
        document.getElementById('loginSection').style.display='block';
        document.getElementById('dashboard').style.display='none';
      }
      else if(section==='dashboard'){
        let curruser=localStorage.getItem('curruser');
        if(curruser){
          document.getElementById('loginSection').style.display='none';
          document.getElementById('dashboard').style.display='block';
          showdetails();
        }
        else{
          alert('Please login first');
        }
      }
    }

    function login(){
      let founduser=null;
      let acc=document.getElementById('accountnumber').value;
      let p=document.getElementById('pswd').value;

      for(let i=0;i<users.length;i++){
        if(users[i].account===acc && users[i].p===p){
          founduser=users[i];
          alert('LOGIN SUCCESSFUL');
          break;
        }
      }

      if(founduser!==null){
        localStorage.setItem('curruser',JSON.stringify(founduser));
        localStorage.setItem('users',JSON.stringify(users));
        document.getElementById('loginSection').style.display='none';
        document.getElementById('dashboard').style.display='block';
        showdetails();
      }
      else{
        alert('Invalid account/password');
      }
    }

    function showdetails(){
      let c=JSON.parse(localStorage.getItem('curruser'));
      if(c){
        document.getElementById('output').innerHTML='Balance: ₹'+c.balance+'<br>Account: '+c.account;
      }
    }

    function deposit(){
      let c=JSON.parse(localStorage.getItem('curruser'));
      let u=JSON.parse(localStorage.getItem('users'));
      let amount=parseInt(document.getElementById('dep').value);

      if(amount%100===0 && amount>0){
        c.balance=c.balance+amount;

        for(let i=0;i<u.length;i++){
          if(u[i].account===c.account){
            u[i].balance=c.balance;
          }
        }

        localStorage.setItem('curruser',JSON.stringify(c));
        localStorage.setItem('users',JSON.stringify(u));
        alert('Balance updated: ₹'+c.balance);
        showdetails();
      }
      else{
        alert('Amount invalid');
      }
    }

    function withdraw(){
      let c=JSON.parse(localStorage.getItem('curruser'));
      let u=JSON.parse(localStorage.getItem('users'));
      let amount=parseInt(document.getElementById('wid').value);

      if(amount%100===0 && amount>0 && amount<=c.balance){
        c.balance=c.balance-amount;

        for(let i=0;i<u.length;i++){
          if(u[i].account===c.account){
            u[i].balance=c.balance;
          }
        }

        localStorage.setItem('curruser',JSON.stringify(c));
        localStorage.setItem('users',JSON.stringify(u));
        alert('Withdrawal successful. Remaining balance: ₹'+c.balance);
        showdetails();
      }
      else{
        alert('Invalid withdrawal amount');
      }
    }

    window.onload=function(){
      let curruser=localStorage.getItem('curruser');
      if(curruser){
        document.getElementById('loginSection').style.display='none';
        document.getElementById('dashboard').style.display='block';
        showdetails();
      }
    }
  </script>

</body>
</html>
```
