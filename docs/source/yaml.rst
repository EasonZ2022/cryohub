Creating/editing tools
======================

In cryoHub, all the available tools (commands) can be found in the ``Command Runner`` section: [image]

In the file system, they are controlled by the YAML files in the directory
``cryohub-react/cryohub/commands/``.

By simply adding a new YAML file written for your own tool in this folder,
cryoHub will generate a corresponding GUI for you. You can also edit the existing
YAML files so that it suits your needs better.


Rules
-----
1. The added tool needs to be able to run from the command line.

2. cryoHub follows RELION's convention for project and job organization, for example: ``<project name>/Import/job001``

3. The command will be executed under the project directory.

4. If there is any files being outputted, an argument indicate the output directory will need to be specified. cryoHub will set this as ``./<command name>/jobxxx`` by default.


Example
-------

Here is a snippet of an example yaml file::

    name: MotionCorr
    custom_name: Motion Correction (RELION 3.1)
    command: mpirun -np 32 -oversubscribe relion_run_motioncorr_mpi
    queue_id: cpu
    postprocess: echo ./corrected_micrographs.star
    file_postprocess: ls
    arguments:
      - name: Input file
        arg: --i
        level: basic
        arg_type: file_path
        description: STAR file with all input micrographs, or a Linux wildcard with all micrographs to operate on

      - name: Output directory
        arg: --o
        level: basic
        arg_type: output_path
        description: Name for the output directory

      - name: Number of threads
        arg: --j
        level: advanced
        arg_type: int
        description: Number of threads per movie (= process)
        default: 1

The resulting UI in the ``Command Runner`` is: [image]


By clicking ``Run``, the command ``command`` will be executed from the project directory.


Detailed description of the YAML file
-------------------------------------

Overall
~~~~~~~

``name``:

``custom_name``:

``command``:

``queue_id``:

``postprocess``:

``file_postprocess``:


Arguments
~~~~~~~~~

``name``:

``arg``:

``level``:

``arg_type``:

``description``:

``default``:
