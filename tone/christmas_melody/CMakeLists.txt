add_executable(pico_tone
    pico_tone.c
)

# Add pico_stdlib library which aggregates commonly used features
target_link_libraries(pico_tone pico_stdlib hardware_pwm)

# Create map/bin/hex/uf2 file in addition to ELF.
pico_add_extra_outputs(pico_tone)

# add url via pico_set_program_url
example_auto_set_url(pico_tone)
