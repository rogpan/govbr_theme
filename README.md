# CSS MENU DROPDOWN 5 NÍVEIS
/* Estilo base do menu da barra lateral esquerda */
.barra-lateral-esquerda ul.menu {
  list-style: none;
  padding: 0;
  margin: 0;
  background-color: #ffffff; /* fundo branco no menu principal */
  border-radius: 5px;
}

.barra-lateral-esquerda ul.menu li {
  position: relative;
}

.barra-lateral-esquerda ul.menu li a {
  display: block;
  font-size: 0.9rem;
  color: #333333; /* texto escuro */
  padding: 10px 15px;
  text-decoration: none;
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
  transition: background-color 0.2s ease-in-out;
  background-color: transparent;
}

.barra-lateral-esquerda ul.menu li a:hover {
  background-color: #e6e6e6; /* cinza escuro suave no hover */
}

/* Submenus: escondidos inicialmente */
.barra-lateral-esquerda ul.menu li ul {
  display: none;
  position: absolute;
  top: 0;
  left: 100%;
  background-color: #ffffff;
  padding: 0;
  margin: 0;
  min-width: 200px;
  border-radius: 5px;
  z-index: 999;
}

/* Mostra submenu ao passar o mouse */
.barra-lateral-esquerda ul.menu li:hover > ul {
  display: block;
}

/* Subníveis adicionais (nível 2, 3, 4, 5) */
.barra-lateral-esquerda ul.menu li ul li {
  position: relative;
}

.barra-lateral-esquerda ul.menu li ul li ul {
  display: none;
  position: absolute;
  top: 0;
  left: 100%;
  background-color: #ffffff;
  min-width: 200px;
  border-radius: 5px;
  z-index: 999;
}

/* Mostra o terceiro nível ao passar o mouse sobre o segundo */
.barra-lateral-esquerda ul.menu li ul li:hover > ul {
  display: block;
}

/* Estilo dos links nos submenus */
.barra-lateral-esquerda ul.menu li ul li a {
  color: #333333; /* texto escuro */
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
  padding: 10px 15px;
  background-color: transparent;
}

.barra-lateral-esquerda ul.menu li ul li a:hover {
  background-color: #e6e6e6;
}

/* Indicador de submenu */
.barra-lateral-esquerda ul.menu li.menu-item--expanded > a::after {
  content: "▶";
  float: right;
  font-size: 0.7em;
  margin-left: 5px;
  color: #999;
}

/* Ajuste responsivo (opcional): quebra submenu para baixo em telas pequenas */
@media (max-width: 768px) {
  .barra-lateral-esquerda ul.menu li ul {
    position: relative;
    left: 0;
    top: auto;
    background-color: #f7f7f7;
    margin-left: 15px;
  }

  .barra-lateral-esquerda ul.menu li ul li ul {
    position: relative;
    left: 0;
    top: auto;
    margin-left: 15px;
  }
}

/* Quarto nível */
.barra-lateral-esquerda ul.menu li ul li ul li ul {
  display: none;
  position: absolute;
  top: 0;
  left: 100%; /* abre ao lado do terceiro */
  background-color: #ffffff;
  min-width: 200px;
  border-radius: 5px;
  z-index: 999;
}

/* Mostra o quarto nível ao passar o mouse sobre o terceiro */
.barra-lateral-esquerda ul.menu li ul li ul li:hover > ul {
  display: block;
}

/* Quinto nível */
.barra-lateral-esquerda ul.menu li ul li ul li ul li ul {
  display: none;
  position: absolute;
  top: 0;
  left: 100%; /* abre ao lado do quarto */
  background-color: #ffffff;
  min-width: 200px;
  border-radius: 5px;
  z-index: 999;
}

/* Mostra o quinto nível ao passar o mouse sobre o quarto */
.barra-lateral-esquerda ul.menu li ul li ul li ul li:hover > ul {
  display: block;
}
