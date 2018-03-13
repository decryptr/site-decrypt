+++
title = "Get the key"
description = "Our free web service requires a free key. You can get one by filling the form below. Please describe clearly what you will do using this service, you must not violate the terms of usage of the decryptr web-service."
+++

<form name="get-key" method="POST" netlify>
  <p>
    <label>Your Name: <input type="text" name="name"></label>   
  </p>
  <p>
    <label>Your Email: <input type="email" name="email"></label>
  </p>
  <p>
    <label>Endpoint: 
      <select name="endpoint">
        <option value="rfb">RFB</option>
      </select>
    </label>
  </p>
  <p>
    <label>What's your purpose on using this API? <textarea name="message"></textarea></label>
  </p>
  <p>
    <label>
      <input type="checkbox" name="accept-terms-service" value="yes"> I agree with the <a href = "/terms-of-service">terms of service</a>.  
    </label>
  </p>
  
  <p>
    <button type="submit">Send</button>
  </p>
</form>