<script>
    export let index;
    export let name;

    const id = `collapse${index}`;
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
        </div>
    </div>
</div>
