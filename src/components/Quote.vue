<template>
    <div class="col-12">
        <div class="jumbotron panel panel-default">
            <div class="panel-body quote">
                <slot></slot>
            </div>
        </div>
    </div>
</template>


<script>
</script>

<style scoped>
    .jumbotron {
        margin:10px;
        padding:5px; 
    }
    .panel-body {
        font-size: 24px;
        color: #2f443b;
    }
    .quote {
       cursor: pointer; 
    }

    .quote:hover {
        background-color: #8aca92;
    }
</style>
