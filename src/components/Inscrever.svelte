<script>
    import {admin_tab} from '../stores/stores.js'
    let _admin_tab;
	admin_tab.subscribe(value => {
		_admin_tab = value;
	});
    
    let avatar, fileinput;
    import { nameList } from "./MemberList.svelte";
    let newMemberName = "";
    const onFileSelected = (e) => {
        let image = e.target.files[0];
        let reader = new FileReader();
        reader.readAsDataURL(image);
        reader.onload = (e) => {
            avatar = e.target.result;
        };
    };

    function signup() {
        console.log(newMemberName);
        nameList.push(newMemberName);
        console.log(nameList);
    }
</script>

<main>
    <div class="shadow-none p-3 m-3 bg-light rounded">
        <h2 align="center">Formulário de inscrição</h2>
        <label for="nome" class="form-label">Nome Completo</label>
        <input
            bind:value={newMemberName}
            type="text"
            class="form-control"
            id="nome"
        />

        <div class="mb-3">
            <label for="morada" class="form-label">Morada</label>
            <input type="text" class="form-control" id="morada" />
            <div class="mb-3">
                <label for="number" class="form-label">Telemóvel/Telefone</label
                >
                <input type="number" class="form-control" id="number" />
                <div class="mb-3">
                    <label for="date" class="form-label"
                        >Data de nascimento</label
                    >
                    <input type="date" class="form-control" id="date" />
                </div>
                <div class="mb-3">
                    <label for="email" class="form-label"
                        >Endereço de Email</label
                    >
                    <input
                        type="email"
                        class="form-control"
                        id="email"
                        placeholder="name@example.com"
                    />
                </div>
                Sexo
                <div class="mb-3">
                    <select class="form-select" aria-label="Sexo">
                        <option value="1">Feminino</option>
                        <option value="2">Masculino</option>
                        <option value="3">Outro</option>
                    </select>
                </div>

                <div class="mb-3">
                    <label for="aboutme" class="form-label">Biografia</label>
                    <textarea
                        class="form-control"
                        id="exampleFormControlTextarea1"
                        rows="3"
                    />
                </div>

                <div id="app">
                    {#if avatar}
                        <img class="avatar" src={avatar} alt="d" />
                    {:else}
                        <img
                            class="avatar"
                            src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                            alt="Default Avatar"
                        />
                    {/if}
                    <input
                        type="image"
                        class="upload"
                        src="https://static.thenounproject.com/png/625182-200.png"
                        alt="Submeter imagem"
                        on:click={() => {
                            fileinput.click();
                        }}
                    />
                    Fotografia de Escuteiro
                    <input
                        style="display:none"
                        type="file"
                        accept=".jpg, .jpeg, .png"
                        on:change={(e) => onFileSelected(e)}
                        bind:this={fileinput}
                    />
                </div>
                <!-- Button trigger modal -->
                <button
                    on:click={signup}
                    type="button"
                    class="btn btn-primary"
                    data-bs-toggle="modal"
                    data-bs-target="#exampleModal"
                >
                    Inscrever
                </button>

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
                                <h1
                                    class="modal-title fs-5"
                                    id="exampleModalLabel"
                                >
                                    Sucesso!
                                </h1>
                                <button
                                    type="button"
                                    class="btn-close"
                                    data-bs-dismiss="modal"
                                    aria-label="Close"
                                />
                            </div>
                            <div class="modal-body">
                                Membro inscrito com sucesso!
                            </div>
                            <div class="modal-footer">
                                <button
                                    type="button"
                                    data-bs-dismiss="modal"
                                    class="btn btn-primary"
                                    on:click={()=>admin_tab.update(()=>"lista")}
                                    >Ver lista de membros</button
                                >
                                <!-- TODO: Meter este botao a dar redirect para a lista de membros -->
                            </div>
                        </div>
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
