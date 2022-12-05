<template>
    <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <div class="close-btn">
                        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                    </div>
                    <h1 class="modal-title fs-5" id="exampleModalLabel">{{ title }}</h1>
                    <hr />
                </div>
                <div class="modal-body">
                    <p>{{ body }}</p>
                </div>
                <div class="modal-footer">
                    <button
                        type="button"
                        class="btn"
                        data-bs-dismiss="modal"
                        onclick="window.location.href='https://www.google.com';">
                        Read more
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ExploreModal',
    props: {
        title: String,
        body: String,
    }
}
</script>

<style scoped>
.modal {
    color: black;
    width: 75%;
    top: 50px;
    left: 50px;
    height: auto;
}

.modal-header {
    flex-flow: column nowrap;
    border-bottom: none;
}

.modal-header h1 {
    font-size: 2rem !important;
    font-family: 'Libre Bodoni', serif;
    color: #611818;
}

.close-btn {
    display: flex;
    justify-content: flex-end;
    width: 100%;
}

.btn-close[aria-label] {
    color: #611818;
}

.modal-title, .modal-body, .modal-footer {
    width: 100%;
    display: flex;
    justify-content: flex-start;
}

.modal-body {
    text-align: left;
    border-bottom: none !important;
}

.modal-body p {
    font-size: .75rem;
}

.modal-footer {
    border-top: none !important;
}

.btn {
    background: linear-gradient(to right, #611818, #9f5252);
    color: white;
}

@media (min-width: 692px) {
    .modal {
        width: 650px;
        top: 150px;
    }

    .modal-body p {
        font-size: 1rem;
    }
}
</style>