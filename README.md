<h1>FREEGPT</h1>
<img style="width:150px;" src="https://i.ibb.co/kqkwx1h/Pics-Art-12-01-04-58-04.png">
<h2>Introduction</h2>
<p>FREEGPT is a <b>JavaScript</b> library made for educational purposes that allows any user to include OpenAI's CHAT-GPT model in their website.</p>
<p>The creator of this library is not responsible for any innapropiate or illegal use of this library, since this project is made to educate about the possibilities of including an AI model into a website.</p>
<p style="color:red" alt="FREEGPT logo" title="FREEGPT logo"><b>NOTE:</b> The project will be removed if any legal restriction is presented.</p>

<h2>Installation</h2>

<p>To include the library in your website just download the script and insert it by using a <code>script</code> tag. For example:</p>

```html
<script src="FREEGPT.js"></script>
```

[Download the file](https://github.com/santiagomirantes/freegpt/blob/main/FREEGPT.js)

<h2 id="usage">Usage</h2>

<p>To start making request with FREEGPT you only have to know one function: <code>FREEGPT.talk()</code>. The syntax is the following:</p>

```js
FREEGPT.talk(query,model)
```
<p>Here is a list of the parameters with their due usage:</p>

<ul>
  <li><b>query:</b> is the message you want to give to ChatGPT. Example: <i>Tell me one country that starts with the letter A.</i></li>
  <li><b>model (optional):</b> is the number of the API you want to use. Right now FREEGPT has two models (see table below) but i´m looking forward to add more. This field must be a number and the default model is 1.</li>
  
</ul>

<h3>Models table:</h3>

<table>
  <tr>
    <td></td>
    <td>Chatbot ji1z</td>
    <td>ChatGPT spanish (works in other languages)</td>
  </tr>
  <tr>
    <td>Model ID</td>
    <td>1</td>
    <td>2</td>
  </tr>
  <tr>
    <td>Current state</td>
    <td>Working</td>
    <td>Working</td>
  </tr>
  <tr>
    <td>GPT</td>
    <td>3.5</td>
    <td>3.5</td>
  </tr>
  <tr>
    <td>Restrictions</td>
    <td>Open AI terms</td>
    <td>Open AI terms</td>
  </tr>
  <tr>
    <td>Generations limit</td>
    <td>No</td>
    <td>No</td>
  </tr>
  <tr>
    <td>Use of proxies</td>
    <td>No</td>
    <td>Yes</td>
  </tr>
</table>

<p><b>Note:</b> FREEGPT works with two proxies, if one of them doesn´t work you can use the other by changing the <code>FREEGPT.proxyUsed</code> property to <code>1</code>.
To check which proxies are working execute the <code>FREEGPT.tryProxies()</code> integrated function like this:</p>

```js
FREEGPT.tryProxies(/*some url*/,0)
```

<p>This function will update the <code>FREEGPT.proxyUsed</code> property automatically.</p>

<p>The <code>talk</code> function returns a promise which you can handle by multiple methods. Two possible methods to handle it are:</p>

<h3>Obtaining the answer via .then</h3>

<p>Just like:</p>

```js
FREEGPT.talk("Hello!",1).then(res => {
    console.log(res)
})
```

<h3>Obtaining the answer via async/await</h3>

<p>Just like:</p>

```js
async function interact(q) {
   let request = await FREEGPT.talk(q,2)
   console.log(request)
}

interact("Make me a list of 10 colors")
```


<p>If the request is rejected, the promise will return <code>undefined</code> and log an error message.</p>


<h2>License</h2>

<p>This project is under the MIT License. Santiago Miranntes, the creator of this library, does not make himself responsible for any incorrect usage of this code.</p>
