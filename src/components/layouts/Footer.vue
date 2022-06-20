<template>
    
    <footer id="footer" class="footer text-center ">

        <div class="text-center p-3">

            <div>
                <div>
                    <a href="https://github.com/Trevor-Uehlin"><i class="fa fa-github"></i></a>
                    <a href="https://www.linkedin.com/in/trevor-uehlin/"><i class="fa fa-linkedin"></i></a>
                    <a href="https://github.com/ocdladefense"><i class="fa fa-github"></i></a> 
                </div>
            </div>

            © 2020 Copyright:
            <a class="" href="/">trevoruehlin.com</a>

        </div>

    </footer>

</template>

<script lang="ts">
import { library } from '@fortawesome/fontawesome-svg-core'
import { faHatWizard } from '@fortawesome/free-solid-svg-icons'
library.add(faHatWizard)
export default {
    components:{

    }
}

</script>

<style scoped>
.footer{
    background-color: blue;
    color:white;
}
a{
    text-decoration: none;
}
</style>