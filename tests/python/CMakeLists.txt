SET(${PROJECT_NAME}_PYTHON_TESTS
  test_talos_walk_contacts
  test_talos_walk_path
  test_rbprm_state_6d
  test_rbprm_state_3d
  )

FOREACH(TEST ${${PROJECT_NAME}_PYTHON_TESTS})
  ADD_PYTHON_UNIT_TEST("py-${TEST}" "tests/python/${TEST}.py")
  SET_TESTS_PROPERTIES("py-${TEST}" PROPERTIES RUN_SERIAL "ON")
ENDFOREACH(TEST ${${PROJECT_NAME}_PYTHON_TESTS})
