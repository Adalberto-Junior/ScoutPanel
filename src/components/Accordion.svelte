<script>
    export let index;
    export let name;

    const id = `collapse${index}`;
    const innerId = `collapseInner${index}`;
</script>

<div class="accordion-item">
    <h2 class="accordion-header" id={`heading${index}`}>
        <button
            class="accordion-button collapsed"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target={`#${id}`}
            aria-expanded="false"
            aria-controls={id}
        >
            <img
                src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                style="width: 50px; height: 50px"
                alt=""
            />
            {name}
        </button>
    </h2>
    <div
        {id}
        class="accordion-collapse collapse"
        aria-labelledby={`heading${index}`}
        data-bs-parent="#accordionExample"
    >
        <div class="accordion-body">
            <div class="table-responsive">
                <table class="table table-borderless">
                    <tbody>
                        <tr>
                            <td>Morada</td>
                            <td>Telemóvel/Telefone</td>
                            <td>Endereço de Email</td>
                        </tr>
                        <tr>
                            <td>Data de nascimento</td>
                            <td>Sexo</td>
                        </tr>
                        <tr>
                            <td>Uma Biografia muito muito muito longa</td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <div class="accordion" id="xd">
                <div class="accordion-item">
                    <h2 class="accordion-header" id="asd">
                        <button
                            class="accordion-button"
                            type="button"
                            data-bs-toggle="collapse"
                            data-bs-target="#qweqwe"
                            aria-expanded="false"
                            aria-controls="qweqwe"
                        >
                            Pagamentos
                        </button>
                    </h2>
                    <div
                        id="qweqwe"
                        class="accordion-collapse collapse"
                        aria-labelledby="asd"
                        data-bs-parent="#xd"
                    >
                        <div class="accordion-body">
                            <ul class="list-group ">
                                <li class="list-group-item d-flex justify-content-between align-items-start">
                                  <div class="ms-2 me-auto">
                                    <div class=""><strong>Dívida trimestral Q1 - </strong>Pago a 21/03</div>
                                  </div>
                                  <span class="badge bg-success rounded-pill">24.99€</span>
                                </li>
                                <li class="list-group-item d-flex justify-content-between align-items-start">
                                  <div class="ms-2 me-auto">
                                    <div class=""><strong>Dívida trimestral Q2 - </strong>Pago a 30/06</div>
                                  </div>
                                  <span class="badge bg-danger rounded-pill">24.99€</span>
                                </li>
                                <li class="list-group-item d-flex justify-content-between align-items-start">
                                  <div class="ms-2 me-auto">
                                    <div class=""><strong>Dívida trimestral Q3 - </strong>Pago a 30/09</div>
                                  </div>
                                  <span class="badge bg-danger rounded-pill">24.99€</span>
                                </li>
                                <li class="list-group-item d-flex justify-content-between align-items-start">
                                    <div class="ms-2 me-auto">
                                        <div class=""><strong>Dívida trimestral Q4 - </strong>Pago a 31/12</div>
                                    </div>
                                    <span class="badge bg-danger rounded-pill">24.99€</span>
                                  </li>
                              </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
