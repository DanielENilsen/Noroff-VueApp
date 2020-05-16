<template>
    <div clss="[ card ]">
        <div class="[ row ]">
            <div class="[ col-sm-4 ]"></div>
        </div>             
        <div class="[card--information]"><br />
            <b> Title: </b>{{title}}<br />  
            <b> Link: </b>{{href}}<br /> 
            <b> Ingredients: </b>{{ingredients}}<br />   
            <b> Image: </b>{{thumbnail}}<br />          
        </div>     

    </div>
</template>

<script>
export default {
    name:"TestMyVue",    
        props:['title','href','ingredients','thumbnail']
}
</script>

