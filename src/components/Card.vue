<template>
    <div class="container">
        <div class="card border-secondary mb-3" style="max-width: 19rem;">
            <div class="card-header text-white bg-dark"><span class="pull-right"><b>Time </b><countdown-timer date="October 2, 2018"></countdown-timer></span></div>
            <div class="card-body text-secondary">
                <h5 class="card-title"><b>Hakan GENC</b></h5>
                <p class="card-text">
                    <b>People</b> <kbd> 2</kbd> <b>Kids</b> <kbd> 2</kbd>
                    <br>
                    <br><b>Room Type</b> <kbd>Suit</kbd>
                </p>
            </div>
            <div class="card-footer bg-transparent border-secondary">
                <kbd style="padding:10px;">Room 34</kbd>
                <button type="button" class="btn btn-danger" data-toggle="modal" data-target=".bd-example-modal-sm">Delete</button>
            </div>
        </div>
        

    <!-- Modalbox -->
    <div class="modal fade bd-example-modal-sm" id="myModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog" role="document">
            <div class="modal-content">
            <div class="modal-header">
                <h1 class="modal-title" id="exampleModalLabel">Are you sure?</h1>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                <span aria-hidden="true">&times;</span>
                </button>
            </div>
            <div class="modal-body">
                Are you sure you want to delete this room? </div>
            <div class="modal-footer">
    
                <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
                <router-link to="/">
                <button type="button" class="btn btn-danger">Delete</button>
                </router-link>
            </div>
            </div>
        </div>
    </div>
    </div>
</template>
<script>
import CountdownTimer from './Timer'
export default {
    name: 'Card',
    components: {
        CountdownTimer
    },
    data() {
        return {

        }
    }
}
</script>

