<script>
   
    
   
    function clear() {  
        //função para limpar os campos!
    }
    export let index;
    

    const id = `${index}`;
    const innerId = `inner${index}`;

    /**
     * Returns a random number between min (inclusive) and max (exclusive)
     */
    function getRandomInt(min, max) {
        min = Math.ceil(min);
        max = Math.floor(max);
        return Math.floor(Math.random() * (max - min + 1)) + min;
    }
</script>

<main>
    <div class="accordion" id="accordionExample{id}">
        <div class="accordion-item">
            <div class="accordion-body">
                <h2 align="center">Minha quota</h2>
                <ul class="list-group">
                    <li
                        class="list-group-item d-flex justify-content-between align-items-start"
                    >
                        <div class="ms-2 me-auto">
                            <div class="">
                                <strong>Dívida trimestral Q1 - </strong>Pago a {getRandomInt(
                                    1,
                                    28
                                )
                                    .toString()
                                    .padStart(2, "0")}/{getRandomInt(1, 3)
                                    .toString()
                                    .padStart(2, "0")}
                            </div>
                        </div>
                        <span class="badge bg-success rounded-pill">24.99€</span
                        >
                    </li>
                    {#if Math.random() < 0.5}
                        <li
                            class="list-group-item d-flex justify-content-between align-items-start"
                        >
                            <div class="ms-2 me-auto">
                                <div class="">
                                    <strong>Dívida trimestral Q2 - </strong>Pago
                                    a {getRandomInt(1, 30)
                                        .toString()
                                        .padStart(2, "0")}/{getRandomInt(4, 6)
                                        .toString()
                                        .padStart(2, "0")}
                                </div>
                            </div>
                            <span class="badge bg-success rounded-pill"
                                >24.99€</span
                            >
                        </li>
                    {:else}
                        <li
                            class="list-group-item d-flex justify-content-between align-items-start"
                        >
                            <div class="ms-2 me-auto">
                                <div class="">
                                    <strong>Dívida trimestral Q2 - </strong>Em
                                    dívida
                                </div>
                                <button
                                  
                                    type="button"
                                    class="btn btn-primary"
                                    data-bs-toggle="modal"
                                    data-bs-target="#exampleModal"
                                >
                                    Pagar
                                </button>
                            </div>
                            <span class="badge bg-danger rounded-pill"
                                >24.99€</span
                            >
                        </li>
                    {/if}

                    <li
                        class="list-group-item d-flex justify-content-between align-items-start"
                    >
                        <div class="ms-2 me-auto">
                            <div class="">
                                <strong>Dívida trimestral Q3 - </strong>Em
                                dívida
                            </div>
                            <button
                                type="button"
                                class="btn btn-primary"
                                data-bs-toggle="modal"
                                data-bs-target="#exampleModal"
                            >
                                Pagar
                            </button>
                        </div>
                        <span class="badge bg-danger rounded-pill">24.99€</span>
                    </li>
                    <li
                        class="list-group-item d-flex justify-content-between align-items-start"
                    >
                        <div class="ms-2 me-auto">
                            <div class="">
                                <strong>Dívida trimestral Q4 - </strong>Em
                                dívida
                            </div>
                            <button
                                type="button"
                                class="btn btn-primary"
                                data-bs-toggle="modal"
                                data-bs-target="#exampleModal"
                            >
                                Pagar
                            </button>
                        </div>
                        <span class="badge bg-danger rounded-pill">24.99€</span>
                    </li>
                </ul>
            </div>
        </div>
        <!-- Modal -->
        <div
            class="modal fade"
            id="exampleModal"
            tabindex="-1"
            aria-labelledby="exampleModalLabel"
            aria-hidden="true"
        >
            <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                        <h1 class="modal-title fs-5" id="exampleModalLabel">
                            Pagamento
                        </h1>
                        <button
                            type="button"
                            class="btn-close"
                            data-bs-dismiss="modal"
                            aria-label="Close"
                        />
                    </div>
                    <div class="modal-body">
                        <label for="card" class="form-label m-1"
                            >Número do cartão</label
                        >
                        <input
                            type="number"
                            class="form-control"
                            id="card"
                            maxlength="16"
                           
                        />
                    </div>
                    <div class="modal-body">
                        <div class="col-md-5">
                            <label for="valid" class="form-label m-1">Validade</label
                            >
                            <input
                                type="month"
                                class="form-control"
                                id="valid"
                                
                            />
                        </div>  
                    </div>
                    <div class="modal-body">  
                        <div class="col-md-3">
                            <label for="cvc" class="form-label m-1">CVC</label
                            >
                            <input
                                type="number"
                                maxlength="3"
                                class="form-control"
                                id="cvc"
                               
                            />
                        </div>
                    </div>
                    <div class="modal-body">
                        <label for="Titular" class="form-label m-1"
                            >Titular do Cartão</label
                        >
                        <input
                            type="text"
                            class="form-control"
                            id="titular"
                            
                        />
                    </div>

                    <div class="modal-footer">
                        <button
                            type="button"
                            data-bs-dismiss="modal"
                            class="btn btn-primary"
                            data-bs-toggle="modal"
                            data-bs-target="#exampleModal2"
                            >Pagar</button
                        >
                    </div>
                </div>
            </div>
        </div>
       <!-- Modal -->
       <div
       class="modal fade"
       id="exampleModal2"
       tabindex="-1"
       aria-labelledby="exampleModalLabel"
       aria-hidden="true"
   >
       <div class="modal-dialog">
           <div class="modal-content">
               <div class="modal-header">
                   <h1 class="modal-title fs-5" id="exampleModalLabel">
                       Aviso!
                   </h1>
                   <button
                       type="button"
                       class="btn-close"
                       data-bs-dismiss="modal"
                       aria-label="Close"
                   />
               </div>
               <div class="modal-body">O Pagamento será processado!</div>
               <div class="modal-footer">
                   <button
                       type="button"
                       data-bs-dismiss="modal"
                       class="btn btn-primary"
                       >OK</button
                   >
               </div>
           </div>
       </div>
   </div>    
</div>
</main>

<style>
    #app {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-flow: column;
    }

    .upload {
        display: flex;
        height: 50px;
        width: 50px;
        cursor: pointer;
    }
    .avatar {
        display: flex;
        height: 200px;
        width: 200px;
    }

    textarea {
        resize: none;
        height: auto;
        overflow-y: hidden;
    }

    textarea:active,
    textarea:focus {
        outline: none;
    }
</style>
