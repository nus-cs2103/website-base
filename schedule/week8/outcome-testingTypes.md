<panel type="danger" header="**`W8.5` Can explain different types of testing** :star:" no-close>

%%**Unit Testing:**%%

<dynamic-panel src="lo-explainUnitTesting.md" type="danger" header="`W8.5a` Can explain unit testing :star:"/>
<dynamic-panel src="lo-useStubs.md" type="info" header="`W8.5b` Can use stubs to isolate an SUT from its dependencies :star::star::star:" />
<dynamic-panel src="lo-explainDependencyInjection.md" type="success" header="`W8.5c` Can explain dependency injection :star::star::star::star:" />
<dynamic-panel src="lo-useDependencyInjection.md" type="success" header="`W8.5d` Can use dependency injection :star::star::star::star:" /><p/>

%%**Integration Testing:**%%

<panel type="warning" header="`W8.5c` Can explain integration testing :star::star:">
  <include src="../../book/testing/testingTypes/integrationTesting/what/full.md" />
  <panel header=":dart: Evidence" expanded>

Explain the difference between unit tests and integration tests. 

  </panel>
</panel>

<panel type="info" header="`W8.5d` Can do integration testing :star::star::star:">
  <include src="../../book/testing/testingTypes/integrationTesting/how/full.md" />
  <panel header=":dart: Evidence" expanded>

Use tests from AddressBook-Level4 to illustrate the difference between unit testings and integration testing. Hint: good examples [`seedu.address.storage.StorageManagerTest`](https://github.com/nus-cs2103-AY1718S1/addressbook-level4/blob/master/src/test/java/seedu/address/storage/StorageManagerTest.java),[`seedu.address.logic.commands.AddCommandTest`](https://github.com/nus-cs2103-AY1718S1/addressbook-level4/blob/master/src/test/java/seedu/address/logic/commands/AddCommandTest.java),[`seedu.address.logic.commands.AddCommandIntegrationTest`](https://github.com/nus-cs2103-AY1718S1/addressbook-level4/blob/master/src/test/java/seedu/address/logic/commands/AddCommandIntegrationTest.java)

  </panel>
</panel><p/>

%%**System Testing:**%%

<panel type="danger" header="`W8.5e` Can explain system testing :star:">
  <include src="../../book/testing/testingTypes/systemTesting/what/full.md" />
  <panel header=":dart: Evidence" expanded>

Explain what system tests are. Give examples from your own project.

  </panel>
</panel>

<panel type="info" header="`W8.5f` Can explain automated GUI testing :star::star::star:">
  <include src="../../book/testing/testAutomation/testingGuis/full.md" />
  <panel header=":dart: Evidence" expanded>

Why is automated testing of GUIs is hard? What can we do about it?

  </panel>
</panel><p/>

%%**Acceptance Testing:**%%

<panel type="warning" header="`W8.5g` Can explain acceptance testing :star::star:">
  <include src="../../book/testing/testingTypes/acceptanceTesting/what/full.md" />
  <panel header=":dart: Evidence" expanded>

Explain what acceptance tests are. Explain how acceptance testing of your project will be done. 

  </panel>
</panel>

<panel type="info" header="`W8.5h` Can explain the differences between system testing and acceptance testing :star::star::star:">
  <include src="../../book/testing/testingTypes/acceptanceTesting/acceptanceVsSystemTesting/full.md" />
  <panel header=":dart: Evidence" expanded>

Explain the difference between system tests and acceptance tests. Explain why both are needed.

  </panel>
</panel><p/>


%%**Alpha/Beta Testing:**%%

<panel type="info" header="`W8.5i` Can explain alpha and beta testing :star::star::star:">
  <include src="../../book/testing/testingTypes/alphaBetaTesting/what/full.md" />
  <panel header=":dart: Evidence" expanded>

Explain alpha and beta testing. How can you do alpha and beta testing in your project?

  </panel>
</panel>


</panel>
