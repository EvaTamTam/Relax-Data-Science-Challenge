# Relax Challenge  
The data is available as two attached CSV files: 

<em> File 1 takehome_user_engagement.csv </em> <br>
<em> File 2 takehome_users.csv </em> <br>
<br>
The data has the following two tables: 
<br>
## Table 1
A user table ( "takehome_users" ) with data on 12,000 users who signed up for the
product in the last two years. This table includes:
<br>
1. name: the user's name <br>
2. object_id: the user's id <br>
3. email: email address <br>
4. creation_source: how their account was created. This takes on one
of 5 values: 
* PERSONAL_PROJECTS: invited to join another user's
personal workspace
* GUEST_INVITE: invited to an organization as a guest
(limited permissions)
* ORG_INVITE: invited to an organization (as a full member)
* SIGNUP: signed up via the website
* SIGNUP_GOOGLE_AUTH: signed up using Google
5. Authentication (using a Google email account for their login
id)
6. creation_time: when they created their account
7. last_session_creation_time: unix timestamp of last login
8. opted_in_to_mailing_list: whether

## Table 2
A usage summary table ("takehome_user_engagement" ) that has a row for each day
that a user logged into the product.
<br>
Defining an "adopted user" as a user who has logged into the product on three separate
days in at least one sevenday period , identify which factors predict future user adoption.

# My Response
Using Gradient Boosting Classifier, I was able to identify the following features from highest importance to lowest:
<html>
<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>GBM</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>creation_source_PERSONAL_PROJECTS</th>
      <td>0.168587</td>
    </tr>
    <tr>
      <th>org_id_0</th>
      <td>0.146781</td>
    </tr>
    <tr>
      <th>org_id_5</th>
      <td>0.111364</td>
    </tr>
    <tr>
      <th>org_id_11</th>
      <td>0.109802</td>
    </tr>
    <tr>
      <th>org_id_1</th>
      <td>0.100078</td>
    </tr>
    <tr>
      <th>org_id_6</th>
      <td>0.083689</td>
    </tr>
    <tr>
      <th>creation_source_GUEST_INVITE</th>
      <td>0.053353</td>
    </tr>
    <tr>
      <th>org_id_12</th>
      <td>0.051296</td>
    </tr>
    <tr>
      <th>creation_source_SIGNUP_GOOGLE_AUTH</th>
      <td>0.029002</td>
    </tr>
    <tr>
      <th>creation_source_ORG_INVITE</th>
      <td>0.020530</td>
    </tr>
    <tr>
      <th>org_id_2</th>
      <td>0.018366</td>
    </tr>
    <tr>
      <th>creation_source_SIGNUP</th>
      <td>0.015320</td>
    </tr>
    <tr>
      <th>org_id_7</th>
      <td>0.015091</td>
    </tr>
    <tr>
      <th>org_id_14</th>
      <td>0.014721</td>
    </tr>
    <tr>
      <th>org_id_13</th>
      <td>0.013943</td>
    </tr>
    <tr>
      <th>opted_in_to_mailing_list</th>
      <td>0.013603</td>
    </tr>
    <tr>
      <th>org_id_16</th>
      <td>0.011248</td>
    </tr>
    <tr>
      <th>enabled_for_marketing_drip</th>
      <td>0.010413</td>
    </tr>
    <tr>
      <th>org_id_4</th>
      <td>0.006296</td>
    </tr>
    <tr>
      <th>invited_by_user_id</th>
      <td>0.003225</td>
    </tr>
    <tr>
      <th>org_id_3</th>
      <td>0.003078</td>
    </tr>
    <tr>
      <th>org_id_10</th>
      <td>0.000212</td>
    </tr>
    <tr>
      <th>org_id_9</th>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>org_id_8</th>
      <td>0.000000</td>
    </tr>
  </tbody>
</table>
</div>
</html>
