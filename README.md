# SpringBoot-React

1] Add cross-origin to spring boot controller.


React Hooks: 
1] useState : to create a temporory state in react to store data 
      a] If state is created using object then while setting the state first destructure the object and then set the set.
      
      //State is always created at the top of the component...and it render's component everytime there is change in state...
      
      import React, {useState} from "react";
      
      
      const [customer,setCustomer] = useState({
        firstName : "",
        lastName : "",
        userName : "",
      })
      
      const saveCustomer = (e) => {
        setState({...customer, firstName : e.target.value})
      }
      
2] useEffect : If we want to perform specific task when page loads...this hook is an alternative for the lifecycle methods of class components.
      (Mostly used for calling the resp API's)
      
      import React , {useEffect} from "react";
      
      const useEffect(() => {
          //Rest API call...
      },[])
      
3] useNavigation: use to navigate between the pages inside react...

      NOTE : BEFORE USING NAVIGATION HOOK SET APP.JS AS FOLLOWS ELSE NAVIGATION HOOK WILL NOT WORK...
   
      import {useNavigation} from "react-router-dom";
      
      const navigate = useNavigate();
      naigate('add-employee');
      
      
      //if parameters are needed to pass...
      navigate(`add-employee/${id}`);
      
      //to collect that parameter in app.js configuration
      
      
      import { BrowserRouter as Router, Routes, Route } from 'react-router-dom'

      <div>
      <Router>
        <div className="container">
          <Routes>
            <Route path="/add-employee/:id" exact element={< AddCustomer />} />
          </Routes>
        </div>
      </Router>
    </div>
 
 
 4] useParams: use to fetch url parameters in another component...
 
      Scenario: in list employee coponent we have update button to update the employee with particular id...whenever someone clicks the update button of particular employee event must get triggred and the page should get navigate to (`/update-employee/${id}`)
      Now in update employee component we will fetch the employee with given id...to get this id inside update-employee component we need useParams hook...
      
      
      import {useParams} from "react-router-dom"
      
      const params = useParams();
     
      now we can fetch id parameter as: params.id
      
      
5] Link is component of react-router-dom which treats link as button but we can use button directly...

5] Axios library is used to make rest calls...


***  LIBRARIES USED ***

1]  npm install bootstrap@latest --save
    //then inside index.js import below two files...
    
    import 'bootstrap/dist/css/bootstrap.min.css';
    import 'bootstrap/dist/js/bootstrap.bundle.min';
    
2] npm install react-router-dom --save

3] npm install axios --save
    
    

      
      
      
      
      
      
