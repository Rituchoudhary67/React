# React

A JavaScript library for building user interfaces

Que1. how to make counter with the help of react 

basic things require while making this assignment:- index.html,index.js,counter.js(which we will make ) 

Step1 :- first thing make one js file in src section (example :- counter.js <---file name)
step2 :- In index.html file looks like 
        <!DOCTYPE html>
         <html lang="en">
            <head>
              <some tags>
              <title>React App</title>
           </head>
           <body>
              <div id="root"></div>

           <script src="../src/index.js"></script>
          </body>
        </html>
Step3 :- In index.js file select the html element by selectors the file looks like this 
  
            import React from 'react';
            import ReactDOM from 'react-dom/client';
            import Counter from './counter';      ----------this is important in that we are inporting Counter file

            const root = ReactDOM.createRoot(document.getElementById('root'));
            root.render(
            <div>
                 <h1>hello</h1>
                 <p>i am ritu learning react</p>
                 <Counter/>                    ----------this is the main step in that we are adding the componet
           </div>
           );

Step4 :- In counter.js file we have to add import react and export default function the file looks like this 
  
         import React from "react"          ----importing react componet
         export default function Counter() {       -----making one function for counter

         let [count,setCount] = React.useState(0);    ---here we r using useState which is a Hook, it allows us to allows us to track                                                              state in a function component(that means when we have to change the                                                                    text,updating it in tha case we are use this because its normally is not updating

         function increase() {                  -----logic for increasing 
            setCount(count + 1);
         }
        function decrease() {                   -----logic for decreasing 
           setCount(count - 1);
        }
       function restart() {                    ------it allways ste zero[0]
          setCount(count = 0);
       }
       return (
        <div>
               <p>{count}</p>                                                -----here the number is going to display
               <button onClick={increase}>Increase Count</button>            -----onClick event for clicking the button
               <button onClick={decrease}>Decrease Count</button>
               <button onClick={restart}>Restart</button>
        </div>
       )
      }


     
