if(CONFIG_SHIELD_ZEN_LEFT OR CONFIG_SHIELD_ZEN_RIGHT)
  zephyr_library()
  zephyr_library_sources_ifdef(CONFIG_PMW3610_ALT drivers/pmw3610_alt/src/pmw3610.c)
endif()
