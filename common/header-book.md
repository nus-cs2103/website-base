<navbar placement="top" type="inverse">
  <a slot="brand" href="{{baseUrl}}/index.html" title="Home" class="navbar-brand">{{ module_pair }} <small>{{ period }}</small></a>
  &nbsp;&nbsp;&nbsp;&nbsp;<md><span class="text-white">Textbook: **Software Engineering for Self-Directed Learners**</span>&nbsp;<span class='badge badge-pill badge-success'>{{ module_pair }} edition - 2018</span></md>
  <li slot="right" class="nav-link">
    <form class="navbar-form">
      <searchbar :data="searchData" placeholder="Search" :on-hit="searchCallback" menu-align-right ></searchbar>
    </form>
  </li>
</navbar>
