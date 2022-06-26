# side effect: any code that effects an outside system
any code that his outputs depends of external data (dependancies for exemple)
///////////////////////////
# how to crate an object 
const name = [{}, {}]
or in the siparate file like this 
export default{
    "name": value,
    "name":{
        "name":[
            {
                "id":"181913649",
                "name":"Dark hotline bling",
            },
        ]
    }
}
in object we need a key which is a unique item 


# lifting state up : 
to pass data from the child to the parent

# use effect:
 it takes 2 parameters the first one is a function a nd the 2nd one is optional . it help us to update the component depend of a outside outuputs
 useEffect(function(){},[parameter])
# get data from api 'fetch':
fetch("anylink")
      .then(res => res.json())
      .then(data => Setname(data.key))
    }
display it : <div>{JSON.stringify(name, null, 2)}</div>
# memory leak: useeffect clean up
we can return a function from useeffect and it will be a cleanup function 
inside of it we add the opposite of what we add inside our useeffect 
for exemple : 
بالعربية عندما يكون عندي زر يظهر ويخفي كومبوننت معينة . وهذيك كومبوننت بدورها يصراو فيها تغيرات .. المشكلة كي منظهرش الكومبوننت يعني ضغطت على زر باش متظهرش (متترندراش) 
فهاذ الحالة افن مترندراتش بصح صرا التغير لي لداخلها بالتالي يصرا ميموري لاك 
useEffect(()=>{
        function watchwidth(){setwindoWith(win)}
        window.addEventListener('resize',watchwidth)
        return function(){window.removeEventListener('resize',watchwidth)}
    },[])
# async function inside useEffect: 
 useEffect(function(){
     async function name(){

     }
     name()
 },[parameter])

 # react router :
1- install the package 
npm install react-router-dom
2- we import it : import {BrowserRouter, Route , Routes} from 'react-router-dom'



 # form in react : 
 1- create a state include all the form data usestate({name:", key:"..})
 2- in the set we will pass 
    ...prev,   //all value
    [name]: type === "checkbox"  ? checked: value,   // new value 
3- prevent default in the submit button 
event.preventDefault()
4-the input : 
<input type="text" 
                    placeholder='FirstName'
                    name='firstname'
                    value={fullname.firstname}
                    onChange={handlerchange}>
            </input>
5- the function it will be like this : 
function handlerchange(e){
     
        return(
            setFullname(prev=>{
                const {name, value, type, checked}=e.target
                return(
                    {
                        ...prev, 
                        [name]: type === "checkbox"  ? checked: value,
                    })
            }
            )
        )
        
    }
# git :
//git-scm.com after install it tip [git --version] to check wich version u are install it
// you can config your info like this : 
[git config --global user.name"...."]
[git config --global user.name"...."]

to see if the info are configer  [git config --list]

** 1-cd to the folder     2-git init (this initialise the folder to be git repo)
initialize the current folder as a git repo
this folder will be the master branch

3- git status "current status of the folder
4-git add . (. means all the folder) to add our files to git repo
(gid add <files/folder>)> adding them to staging area
4- git commit -m "here the comment" >

git log--oneline (see a brief log of the commits)
git checkout <commint number><file > checkout the file from an oloder commit
git reset (reset the staging area to the last commit )

get clone url to create a copy of any repo

