# TSGenerics
### A study on TypeScript Generics.

This is surprisingly simple actually. You can use this whenever you are not quite sure yet about the type that you will be working with.
 
 ## Generic interface sample
 
 interface Todo<T>{
    id: T;
    taskName: string;
 }
 
 const todo1: Todo<string> = {
    id: "t123",
    taskName: "feed cat 🐱"
 }
 
 const todo2: Todo<number> = {
     id: 999,
    taskName: "feed cat 🐱"
 }
 
 ### With Generics, you can assign the type dynamically, depending on what you need.
 For me though, this works really well with React states.
 
 ## React with Generics
 
 const SampleComponent: React.FC = () => {
    const [todos, setTodos] = useState<Todo[]>([]) // this essentially tells us that the state will be looking for a Todo array. It will specifically look for an array of objects that has the form of the Todo interface we created.

}
