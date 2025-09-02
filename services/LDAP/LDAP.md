<h1>LDAP : (Lightweight Directory Access Protocol)</h1>
LDAP {Lightweight Directory Access Protocol} is an open, vendor-neutral application protocol for accessing and maintaining distributed directory information services over a network. It acts as a standardized communication language that allows applications and users to find and verify information like usernames, passwords, and other user attributes stored in a central directory service. A directory service is essentially a network-based phonebook for resources like users, groups, and devices, and LDAP provides the mechanism to query, retrieve, and manage this data efficiently. 

<br>
</br>
<b>Vendor-neutral</b> = Software/Hardware that can be used with variety of plateforms, softwares and hardwares. 
<br>
</br>

<table>
  <tr>
     <td>
Port  </td>
    <td>Protocol</td>
  <td>
Description  </td>
  </tr>
  <tr>
    <td>389</td>
    <td>TCP/UDP</td>
    <td>Standard LDAP. Unencrypted by default. Can support STARTTLS for optional encryption.</td>
  </tr>
  <tr>
    <td>636</td>
    <td>TCP</td>
    <td>LDAPS (LDAP over SSL/TLS). Fully encrypted from the start of the connection.
</td>
  </tr>
 
</table>
<br>
</br>

<h2>Authentication Process:</h2>
<img src=https://github.com/bhuwanpatidar/Kalki_2.0/blob/main/services/LDAP/new.jpeg > </img>
<img src=https://github.com/bhuwanpatidar/Kalki_2.0/blob/main/services/LDAP/new.png > </img>

<h3>Summary Auth:</h3>
<p>
  <dl>
    <dt>1. User Initiates Login</dt>
    <dd> The user enters their credentials (username and password) into an application or service.</dd
    <dt> 2. Client Resolves Distinguished Name (DN)
    </dt>
    <dd> The client application converts the user's simple identifier (e.g., username or email) into a Distinguished Name (DN). This is achieved by performing a search query against the LDAP directory to find the full DN associated with the provided identifier.

For example, a search filter might look like: (uid=username) or (mail=email@example.com). 
Connect2id
</dd>

  <dt>3. Establish Connection to LDAP Server
</dt>
    <dd> The client establishes a connection to the LDAP server, typically over port 389 (unencrypted) or 636 (LDAPS – encrypted).

It's recommended to use LDAPS to ensure the security of the credentials during transmission. 
JumpCloud
</dd>

  <dt>4. Client Sends Bind Request</dt>
 
  The client sends a "bind" request to the LDAP server. <br>
      
          •Simple Bind: The client provides the full DN and password.
          •SASL Bind: Utilizes the Simple Authentication and Security Layer for more complex authentication mechanisms. 
        

<dt>5. LDAP Server Verifies Credentials</dt>
    <dd> The LDAP server checks the provided DN and password against its directory entries.

If the credentials are correct, the server returns a success response.

If the credentials are incorrect, the server returns an error response, such as "Invalid Credentials" (LDAP error code 49). </dd

<dt>6. Authentication Result</dt>
    <dd> Success: The client is authenticated and granted access to the requested resources.

Failure: The client is denied access, and the application may prompt the user to re-enter their credentials.</dd>

  </dl> 
</p>

<br>
</br>
<h2>Working Process:</h2>
<img src=https://github.com/bhuwanpatidar/Kalki_2.0/blob/main/services/LDAP/new2.png > </img>

<br>
</br>
<h2> Attacking LDAP :</h2>












<br>
</br>
<br>
</br>
