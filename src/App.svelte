<script>
    import Home from "./components/Home.svelte";
    import Admin from "./components/Admin.svelte";

    var main_tab = "home";
    let admin_mode = true;
    let textSelected = "text";
</script>

<main>
    <div
        style="height: 100%; width: 20%; position: absolute; top: 0; left: 0; overflow: auto"
    >
        <div class="shadow-none p-3 m-3 bg-light rounded">
            <a
                href="#"
                class="nav-link"
                style="display: block"
                on:click={() => (main_tab = "home")}>ScoutPanel</a
            >
        </div>
        <div class="shadow-none p-3 m-3 bg-light rounded">
            <a
                href="#"
                class="nav-link"
                style="display: block"
                on:click={() => (main_tab = "perfil")}>Perfil</a
            >
        </div>
        <div class="shadow-none p-3 m-3 bg-light rounded">
            <a
                href="#"
                class="nav-link"
                style="display: block"
                on:click={() => (main_tab = "notificacoes")}>Notificações</a
            >
        </div>
        {#if admin_mode == true}
            <div class="shadow-none p-3 m-3 text-bg-success rounded">
                <a
                    href="#"
                    class="nav-link"
                    style="display: block"
                    on:click={() => (main_tab = "admin")}>Admin</a
                >
            </div>
        {/if}
        <div class="shadow-none p-3 m-3 bg-light rounded">
            <a
                href="#"
                class="nav-link"
                style="display: block"
                on:click={() => (main_tab = "definicoes")}>Definições</a
            >
        </div>
        <div class="shadow-none p-3 m-3 bg-light rounded">
            <a
                href="#"
                class="nav-link"
                style="display: block"
                on:click={() => (main_tab = "pagamentos")}>Pagamentos</a
            >
        </div>
        <div class="shadow-none p-3 m-3 text-bg-primary rounded">
            <a
                href="#"
                class="nav-link"
                data-bs-toggle="modal"
                data-bs-target="#publishModal"
                style="display: block">Publicar</a
            >
        </div>
        <div class="form-check form-switch m-3">
            <input
                class="form-check-input"
                type="checkbox"
                role="switch"
                id="flexSwitchCheckChecked"
                bind:checked={admin_mode}
            />
            <label class="form-check-label" for="flexSwitchCheckChecked"
                >Modo de Administrador</label
            >
        </div>
    </div>
    <div
        style="height: 100%; width: 80%; position: absolute; top: 0; right: 0;"
    >
        {#if main_tab == "home"}
            <Home />
        {:else if main_tab == "admin"}
            <Admin />
        {/if}
    </div>
</main>

<!-- Modal -->
<div
    class="modal fade"
    id="publishModal"
    tabindex="-1"
    aria-labelledby="publishModalLabel"
    aria-hidden="true"
>
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <div
                    class="btn-group"
                    role="group"
                    aria-label="Basic radio toggle button group"
                    id="asd"
                >
                    <input
                        type="radio"
                        class="btn-check"
                        name="btnradio"
                        id="btnradio1"
                        bind:group={textSelected}
                        value={"text"}
                        autocomplete="off"
                        checked
                    />
                    <label class="btn btn-outline-primary" for="btnradio1"
                        >Texto</label
                    >

                    <input
                        type="radio"
                        class="btn-check"
                        name="btnradio"
                        id="btnradio2"
                        bind:group={textSelected}
                        value={"media"}
                        autocomplete="off"
                    />
                    <label class="btn btn-outline-primary" for="btnradio2"
                        >Media</label
                    >

                    <input
                        type="radio"
                        class="btn-check"
                        name="btnradio"
                        id="btnradio3"
                        bind:group={textSelected}
                        value={"poll"}
                        autocomplete="off"
                    />
                    <label class="btn btn-outline-primary" for="btnradio3"
                        >Votação</label
                    >
                </div>
                <button
                    type="button"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                />
            </div>

            <div class="modal-body">
                <input
                    type="text"
                    class="form-control"
                    id="nome"
                    placeholder="Descrição"
                />
                {#if textSelected == "media"}
                    <div class="mb-3">
                        <label for="formFile" class="form-label"
                            >Arrastar ou <strong>submeter</strong> imagens/videos</label
                        >
                        <input
                            class="form-control"
                            type="file"
                            id="formFile"
                            accept="image/png, image/jpeg, video/mp4 ,video/x-m4v, video/*"
                            multiple
                        />
                    </div>
                {/if}
            </div>
            <div class="modal-footer">
                <button
                    type="button"
                    class="btn btn-primary"
                    data-bs-dismiss="modal">Publicar</button
                >
            </div>
        </div>
    </div>
</div>
