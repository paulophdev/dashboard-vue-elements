<template>
  <section
    class="content w-full py-7 px-4 bg-white flex justify-center rounded-lg"
  >
    <div class="caixa-input-100">
      <div class="flex justify-between">
        <h1 class="form-title">Cadastro Clientes</h1>
        <div class="form-options">
          <button class="btn-success" disabled>E <span>Editar</span></button>
          <button class="btn-danger">X <span>Excluir</span></button>
          <button class="btn-secondary">V <span>Fechar</span></button>
        </div>
      </div>

      <form>
        <div class="caixa-input-100">
          <label>Nome</label>
          <input placeholder="Nome" class="input-text" />
        </div>

        <div class="caixa-input-50">
          <label>E-mail</label>
          <input placeholder="E-mail" type="email" class="input-text" />
        </div>

        <div class="caixa-input-25">
          <label>Senha</label>
          <input placeholder="Senha" type="password" class="input-text" />
        </div>

        <div class="flex justify-between flex-wrap caixa-input-100">
          <div class="flex flex-col">
            <label for="">Inicio</label>
            <input placeholder="Data" type="date" class="input-text" />
          </div>
          <div class="flex flex-col">
            <label for="">Término</label>
            <input
              placeholder="Data Time"
              type="datetime-local"
              class="input-text"
            />
          </div>
        </div>

        <div class="caixa-input-100">
          <label>Cidade</label>
          <select class="input-text">
            <option value="" selected>Cidades</option>
            <option value="1">Feira de Santana</option>
          </select>
        </div>

        <div class="caixa-input-25">
          <label>Estado</label>
          <select class="input-text">
            <option value="" selected>Estados</option>
            <option value="1">Bahia</option>
          </select>
        </div>

        <div class="caixa-input-25">
          <label>Número</label>
          <input placeholder="Número" class="input-text" />
        </div>

        <div class="caixa-input-50">
          <label>Total</label>
          <input placeholder="Total" type="number" class="input-text" />
        </div>

        <label for="check01"
          ><input id="check01" type="checkbox" /> Opção 01</label
        >
        <label for="check02"
          ><input id="check02" type="checkbox" /> Opção 02</label
        >
        <label for="check03"
          ><input id="check03" type="checkbox" /> Opção 03</label
        >

        <label for=""><input type="radio" name="opt" /> BA</label>
        <label for=""><input type="radio" name="opt" /> SP</label>
        <label for=""><input type="radio" name="opt" /> AL</label>

        <button class="btn-primary w-60">Nome do Button</button>
      </form>
    </div>
  </section>
</template>
