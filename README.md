# Graph API  // Odyssey Week 7

### Rocket Elevators New API : GraphQL
</br>

### **How to answer the 3 questions :** 
</br>

#### Go to the GraphiQL interface : http://skyrock.ml/graphql 
</br>

#### 1- *To get a building address and the start and end intervention times about a specific intervention :* 
In GraphiQL, inside the leftside text field, write : 
```
{
  intervention (id: 199) {
    address{
      street_address
      city
      state
      country
    }
    starttime
    finishtime
  }
}
```
Where you write the specific intervention ID number you want on the first line [ex: '199']. It goes from 1 to 1000. </br>
You can write all or some of the desired address and time items to show. </br>
Press the **PLAY** logo right over the text field. </br>
The answer will appear on the rightside empty panel. 
</br>

#### 2- *To get the client informations and the list of all of the interventions about a specific building :* 
In GraphiQL, inside the leftside text field, write : 
```
{
  building(id:1){
    customer{
      id
      business_name
      contact_full_name
      contact_phone
      contact_email
    }
    interventions {
      id
      starttime
      finishtime
    }
  }
}
```
Where you write the specific intervention ID number you want on the first line [ex: 'id:1']. It goes from 1 to 49. </br>
You can write all or some of the desired address and time items to show. </br>
Press the **PLAY** logo right over the text field. </br>
The answer will appear on the rightside empty panel.
</br>


#### 3- *To get all of the interventions done by a specific employee with all of the buildings associated/related with those employee's interventions, including the buildings details :*
In GraphiQL, inside the leftside text field, write : 
```
{
  employee(id: 4) {
    id
    first_name
    last_name
    email
    title    
    building {
      id
      building_name
      address_id
      customer_id
      administrator_full_name
      administrator_phone
    }
    buildingDetail{
      id
      building_id
      information_key
      value 
    }
    interventions {
      id
      buildingid
      starttime
      finishtime
    } 
  } 
}
```
Where you write the specific intervention ID number you want on the first line [ex: 'id:4']. </br>
You can write all or some of the desired address and time items to show. </br>
Press the **PLAY** logo right over the text field. </br>
The answer will appear on the rightside empty panel.

</br>
</br>
</br>

#### Authors : 
David Boutin, Luna-Victoria Leclerc, Dany Boucher, Dominic Bonneau and Valerie Beaupre 