<h1>FREEGPT</h1>
<img style="width:150px;" src="https://i.ibb.co/kqkwx1h/Pics-Art-12-01-04-58-04.png">
<h2>Introduction</h2>
<p>FREEGPT is a <b>JavaScript</b> library made for educational purposes that allows any user to include OpenAI's CHAT-GPT model in their website.</p>
<p>The creator of this library is not responsible for any innapropiate or illegal use of this library, since this project is made to educate about the possibilities of including an AI model into a website.</p>
<p style="color:red" alt="FREEGPT logo" title="FREEGPT logo"><b>NOTE:</b> The project will be removed if any legal restriction is presented.</p>

<h2 id="usage">Usage</h2>

<p>To start making request with FREEGPT you only have to know one function: <code>FREEGPT.talk()</code>. The syntax is the following:</p>
<code>FREEGPT.talk(query,model)</code>
<p>Here is a list of the parameters with their due usage:</p>

<ul>
  <li><b>query:</b> is the message you want to give to ChatGPT. Example: <i>Tell me one country that starts with the letter A.</i></li>
  <li><b>model (optional):</b> is the number of the API you want to use. Right now FREEGPT only has one API but where are looking forward to add more. This field must be a number and the default model is 1.</li>
  
</ul>

<p>The <code>talk</code> function returns a promise which you can handle by multiple methods. Two possible methods to handle it are:</p>

<h3>Obtaining the answer via .then</h3>

<p>Just like:</p>

<code>
  FREEGPT.talk("Hello!").then(res => {
    console.log(res)
})
</code>

<h3>Obtaining the answer via async/await</h3>

<p>Just like:</p>
<code>
  async function interact(q) {
   let request = await FREEGPT.talk(q)
   console.log(request)
}

interact("Make me a list of 10 colors")
</code>

<h2>License</h2>

<p>This project is under the MIT License. Santiago Miranntes, the creator of this library, does not make himself responsible for any incorrect usage of this code.</p>
