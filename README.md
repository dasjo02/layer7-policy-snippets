<table>
<thead>
<tr>
<th>Policy Name</th>
<th>What does it do?</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/epoch-to-gmt.xml">Epoch to GMT</a></td>
<td>Converts epoch time to a human-readable date/time stamp.</td>
 <td></td>
</tr>
<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/form-based-login.xml">Form based login</a></td>
<td>HTML form based login and authentication using the Gateway as an IDP</td>
 <td></td>
</tr>
<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/302-redirect.xml">302 redirect</a></td>
<td>Send a HTTP 302 to redirect the user agent to another location</td>
 <td></td>
</tr>
<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/substring.xml">Substring</a></td>
 <td>Extract a substring. </td>
 <td>Modify these variables as needed:<br><br>
  <b>STRING:</b> The string to extract the substring from <br>
  <b>START:</b> The starting position <br>
  <b>LEN:</b> Length of characters to extract
</td>
</tr>
<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Retrieve OAuth 2.0 Token.xml">Retrieve OAuth 2.0 Token</a></td>
<td>An example of how to use the MAG Retrieve OAuth 2.0 Token assertion using the Authorization Code grant</td>
 <td></td>
</tr>
<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Random number generator (variable length).xml">Random number generator (variable length)</a></td>
<td>Genearte a random number based on a variable length</td>
 <td></td>
</tr> 
 
<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Add%20XML%20Elements.xml">Add XML Elements</a></td>
<td>Example of the Add XML Elements assertion</td>
 <td>
  <a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Sample XML For adding PRICE element.xml">Sample XML payload for adding PRICE element</a>
</td>
</tr> 

<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Remove XML Elements.xml">Remove XML Elements</a></td>
<td>Example of the Remove XML Elements assertion</td>
 <td>
  <a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Sample XML For removing PRICE element.xml">Sample XML payload for removing PRICE element</a>
</td>
</tr> 

<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Retrieve OAuth 2.0 Token - ROPC.xml">Retrieve OAuth 2.0 Token - ROPC</a></td>
<td>Example of the Retrieve OAuth 2.0 Token assertion using the Resource Owner Password Credentials grant</td>
 <td>
Makes use of the OAuth test client ID and secret. If the test clients are not installed this will need to be modified to an existing ID and secret in your environment.
</td>
</tr> 

<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Retrieve OAuth 2.0 Token - Client Creds.xml">Retrieve OAuth 2.0 Token - Client Creds</a></td>
<td>Example of the Retrieve OAuth 2.0 Token assertion using the Client Credentials grant</td>
 <td>
Makes use of the OAuth test client ID and secret. If the test clients are not installed this will need to be modified to an existing ID and secret in your environment.
</td>
</tr> 


<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/OAuth protected endpoint.xml">OAuth protected endpoint</a></td>
<td>A very simple OAuth protected endpoint</td>
 <td>
</td>
</tr> 

<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Validate JSON schema.xml">Validate JSON schema</a></td>
<td>Example of the Validate JSON Schema assertion</td>
 <td>
  <a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Sample JSON for Validate JSON schema.json">Sample JSON payload</a>
</td>
</tr> 

<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/OTK Session Get Store Delete.xml">OTK Session Get Store Delete</a></td>
<td>Examples of retrieving, storing and deleting OAuth session data</td>
 <td></td>
</tr> 


<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Concatenate JSON.xml">Concatenate JSON</a></td>
<td>Example of concatenating JSON values</td>
 <td>

 </td>
</tr> 


<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/Manipulating variables with the JavaScript assertion.xml">Manipulating variables with the JavaScript assertion</a></td>
 <td>Manipulating variables with the JavaScript assertion (creating and manipulating existing variables)</td>
</tr> 

<tr>
<td><a href="https://github.com/dasjo02/layer7-policy-snippets/blob/master/JWKS.xml">JWKS</a></td>
 <td>Validating a JWT with JWKS</td>
 <td>
  This example uses a Google issued JWT and validates the signature using JWKS. To test with Google: <br><br>
  <ol>
   <li>Navigate to the <a href="https://developers.google.com/oauthplayground">Google OAuth Playground</a> to generate a JWT</li>
   <li>Select any of the available APIs (i.e: Gmail API v1) and in the 'Input your own scopes' box enter <b>openid</b>. Click the 'Authorize APIs' button</li>
   <li>Log in using a Google account</li>
   <li>Review the requested access permissions and authorize access if comfortable with the permissions. You are then returned to the OAuth playground</li>
   <li>Click the 'Exchange authorization code for tokens' button</li>
   <li>An <b>id_token</b> will be returned in the lower pane. Copy this value</li>
   <li>Load the attached policy into Policy Manager</li>
   <li>Locate the JWT context variable and set it to the copied value. Save and Activate the policy</li>
   <li>Navigate to Tasks -> Certificates, Keys and Secrets -> Manage Certificates</li>
   <li>Click the Add button and paste this URL into the 'Retrieve via SSL Connection' field: https://www.googleapis.com</li>
   <li>Accept any warnings and click finish. You can now test the policy by navigating to the endpoint a browser.</li>
  </ol>
  <br>
  To modify this policy for verifying a JWT issued by someone else
  <ol>
   <li>Add the JWT to the policy in the variable named JWT</li>
   <li>Change the route assertion URL to point to your JWKS endpoint</li>
   <li>Add the certificate for the JWKS endpoint to the Gateway</li>
   <li>Modify the 'Look Up Trusted Certificate by Name assertion to use the name displayed for the certificate imported in the previous step</li>
   <li> Save and activate the policy</li>
  </ol>
 </td>
</tr> 

</tbody>
</table>
