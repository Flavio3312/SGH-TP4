# 🏥 Sistema de Gestión Hospitalaria

---

<nav>
  <a href="#" onclick="mostrarFormulario('registro')">Registrar Paciente</a> |
  <a href="#" onclick="mostrarFormulario('consulta')">Consultar Paciente</a> |
  <a href="#" onclick="mostrarFormulario('modificacion')">Modificar Paciente</a> |
  <a href="#" onclick="mostrarFormulario('listado')">Listar Pacientes</a> |
  <a href="#" onclick="mostrarFormulario('baja')">Eliminar Paciente</a>
</nav>

---

<div id="formularios">

  <!-- Registro -->
  <div id="form-registro" style="display:none;">
    <h3>Registrar Paciente</h3>
    <form>
      <input type="text" placeholder="Nombre"><br><br>
      <input type="text" placeholder="Apellido"><br><br>
      <input type="text" placeholder="DNI"><br><br>
      <input type="email" placeholder="Email"><br><br>
      <button type="submit">Aceptar</button>
      <button type="reset">Cancelar</button>
    </form>
  </div>

  <!-- Consulta -->
  <div id="form-consulta" style="display:none;">
    <h3>Consultar Paciente</h3>
    <form>
      <input type="text" placeholder="Nombre"><br><br>
      <input type="text" placeholder="Apellido"><br><br>
      <input type="text" placeholder="DNI"><br><br>
      <input type="email" placeholder="Email"><br><br>
      <button type="submit">Aceptar</button>
      <button type="reset">Cancelar</button>
    </form>
  </div>

  <!-- Modificación -->
  <div id="form-modificacion" style="display:none;">
    <h3>Modificar Paciente</h3>
    <form>
      <input type="text" placeholder="Nuevo Nombre"><br><br>
      <input type="text" placeholder="Nuevo Apellido"><br><br>
      <input type="text" placeholder="Nuevo DNI"><br><br>
      <input type="email" placeholder="Nuevo Email"><br><br>
      <button type="submit">Aceptar</button>
      <button type="reset">Cancelar</button>
    </form>
  </div>

  <!-- Listado -->
  <div id="form-listado" style="display:none;">
    <h3>Listado de Pacientes</h3>
    <p>Aquí se mostrará una tabla con los pacientes registrados.</p>
    <!-- Tabla estática de ejemplo -->
    <table border="1">
      <tr><th>Nombre</th><th>Apellido</th><th>DNI</th><th>Email</th></tr>
      <tr><td>Ejemplo</td><td>Paciente</td><td>12345678</td><td>ejemplo@mail.com</td></tr>
    </table>
    <br>
    <button onclick="ocultarTodo()">Cerrar</button>
  </div>

  <!-- Baja -->
  <div id="form-baja" style="display:none;">
    <h3>Eliminar Paciente</h3>
    <form>
      <input type="text" placeholder="DNI del paciente a eliminar"><br><br>
      <button type="submit">Aceptar</button>
      <button type="reset">Cancelar</button>
    </form>
  </div>

</div>

<script>
  function ocultarTodo() {
    document.getElementById("form-registro").style.display = "none";
    document.getElementById("form-consulta").style.display = "none";
    document.getElementById("form-modificacion").style.display = "none";
    document.getElementById("form-listado").style.display = "none";
    document.getElementById("form-baja").style.display = "none";
  }

  function mostrarFormulario(id) {
    ocultarTodo();
    document.getElementById("form-" + id).style.display = "block";
  }
</script>
