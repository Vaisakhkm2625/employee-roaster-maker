<script>
  import svelteLogo from "./assets/svelte.svg";
  import viteLogo from "/vite.svg";
  import Counter from "./lib/Counter.svelte";

  import DragDropList from "svelte-dragdroplist";
  //https://github.com/jwlarocque/svelte-dragdroplist

let removesItems = true;
let employees = [
        "vaisakh",
        "vrishali",
        "prasanth",
        "aasiq",
        "devi",
        "vineeth",
        "likhith",
        "arun"
        ]


let weeklist = [
        "sunday",
        "monday",
        "tuesday",
        "wednesday",
        "thursday",
        "friday",
        "saturday",
        ]

let shifts = [
        "morning",
        "noon",
        "night"
        ]


let newName = '';

  function addlist() {
    console.log("added");
    employees.push(newName);
  }

  $: console.log(employees)
</script>

  <DragDropList bind:data={employees} {removesItems}/>

  <input bind:value={newName}>
  <button on:click={addlist}>+ </button>



