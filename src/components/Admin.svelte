<script>
    import Inscrever from "./Inscrever.svelte";
    
    var admin_tab = "admin"
</script>

<main>
    <div style="height: 100%; width: 25%; position: absolute; top: 0; left: 0;">
        <div class="shadow-none p-3 mt-3 mb-3 mw-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>admin_tab="admin"}>Administração</a></div>
        <div class="shadow-none p-3 mt-3 mb-3 mw-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>admin_tab="lista"}>Lista de membros</a></div>
        <div class="shadow-none p-3 mt-3 mb-3 mw-3 text-bg-success rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>admin_tab="inscrever"}>Inscrever novo membro</a></div>
        <div class="shadow-none p-3 mt-3 mb-3 mw-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>admin_tab="pedidos"}>Pedidos de requerimentos</a></div>
        <div class="shadow-none p-3 mt-3 mb-3 mw-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>admin_tab="estatisticas"}>Estatísticas</a></div>
    </div>
    <div style="height: 100%; width: 75%; position: absolute; top: 0; right: 0;">
        <div style="height: 95%">
            <div style="height: 100%; overflow: auto">
                {#if admin_tab=="inscrever"}
                    <Inscrever/>
                {:else if admin_tab=="estatisticas"}
                    1
                {/if}
            </div>
        </div>
    </div>
</main>
