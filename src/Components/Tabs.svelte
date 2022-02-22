<script>
    import {createEventDispatcher} from "svelte";
    const dispatch=createEventDispatcher();
    export let tabItems,activeItem;
    import TabItem from "./TabItem.svelte";
    let content=[{
             Time:"Morning",
             Type:'Breakfast',
             Item:"Sandwitch",
             Quantity:3,
     },
     {
             Time:"Afternoon",
             Type:'Lunch',
             Item:"Fried Rice",
             Quantity:2,
     },
     {
             Time:"Night",
             Type:'Dinner',
             Item:"Chapati Dal",
             Quantity:3,
    }
];
</script>
<div class="tab-container">
    <div class="tab-header">
{#each tabItems as item}
    <li on:click={()=>dispatch('tabChange',item)} class:active={item===activeItem}>{item}</li>
{/each}
</div>
<div class="tab-body-container">
<TabItem {content} {activeItem}/>
</div>
</div>
<style>
.tab-container
{
    width:30%;
    height:auto;
    margin: auto;
    margin-top: 10rem;
}
.tab-header
{
    width: 100%;
    display: grid;
    grid-template-columns: repeat(3,1fr);
    border: 2px solid rgb(214, 214, 214);
    border-bottom: 0px;
    color:white;
}
.tab-header li
{
    list-style: none;
    background-color: rgb(155, 55, 248);
    padding: 1.5rem 0rem;
    cursor: pointer;
}
.active
{
    background-color: rgb(249, 249, 250) !important;
    color: rgb(155, 55, 248);
    border: 2px solid rgb(222, 69, 236);
}
.tab-body-container
{
width:100%;
height: 100%;
display: flex;
justify-content: center;
margin-bottom: 1rem;
border: 2px solid rgb(214, 214, 214);
border-top: 0px;
}
</style>