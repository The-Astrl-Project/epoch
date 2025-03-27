# Epoch || meson.build
# --------------------------------
# Meson build configuration.
#
# Authors: @MaxineToTheStars <https://github.com/MaxineToTheStars>
# ----------------------------------------------------------------

# Project declaration
project(
    'epoch',
    'c',
    default_options: {
        'prefix': '/usr',
        'buildtype': 'debug',
        'debug': 'true',
        'default_library': 'shared',
        'errorlogs': 'true',
        'optimization': '0',
        'stdsplit': 'true',
        'c_std': 'gnu99'
    },
    license: 'GPLv3',
    license_files: ['LICENSE'],
    meson_version: '>= 1.5.0',
    version: '0.1.0-dev'
)

# Project variables
PROJECT_VERSION = '0.1.0-dev'

# Run the globber.sh script to collect all source and header files
# NOTE: This is not recommended
# https://github.com/mesonbuild/meson/blob/master/docs/markdown/FAQ.md#but-i-really-want-to-use-wildcards
g_source = run_command('bash', './scripts/globber.sh', '-s', './projects/cli/src', capture: true, check: true)
g_include = run_command('bash', './scripts/globber.sh', '-i', './projects/cli/include', capture: true, check: true)
g_source_files = g_source.stdout().strip().replace('./', '').split('\n')

# EFI declaration
run_command(
    'bash',
    './scripts/generate_pe.sh',
    capture: true,
    check: true
)

# Executable declaration
executable(
    'epochcli',
    'projects/cli/src/epochcli.c',
    include_directories: include_directories('projects/cli/include'),
    install: true,
    sources: g_source_files
)
