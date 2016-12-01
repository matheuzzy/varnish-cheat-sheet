VCL built-in subroutines and their legal returns at the frontend (client) side

| subroutine  | scope  | deliver | fetch | restart | hash | pass | pipe | synth | purge | lookup |
--------------------------------------------------------------------------------------
| vcl_deliver | client |    x    |       |    x    |      |      |      |   x   |       |        |
| vcl_hash    | client |         |       |         |      |      |      |       |       |    x   |
| vcl_hit     | client |    x    |   x   |    x    |      |   x  |      |   x   |       |        |
| vcl_miss    | client |         |   x   |    x    |      |   x  |      |   x   |       |        |
| vcl_pass    | client |         |   x   |    x    |      |      |      |   x   |       |        |
| vcl_pipe    | client |         |       |         |      |      |   x  |   x   |       |        |
| vcl_purge   | client |         |       |    x    |      |      |      |   x   |       |        |
| vcl_recv    | client |         |       |         |   x  |   x  |   x  |   x   |   x   |        |
| vcl_synth   | client |    x    |       |    x    |      |      |      |       |       |        |


VCL built-in subroutines and their legal returns at the backend side


| subroutine           | scope       | fetch | deliver | abandon | retry | ok | fail |
-----------------------------------------------------------------------------
| vcl_backend_fetch    | backend     |   x   |         |    x    |       |    |      |
| vcl_backend_response | backend     |       |    x    |    x    |   x   |    |      |
| vcl_backend_error    | backend     |       |    x    |         |   x   |    |      |
| vcl_init             | vcl.load    |       |         |         |       |  x |   x  |
| vcl_fini             | vcl.discard |       |         |         |       |  x |      |


Variables readable (R) or writable (W) in VCL subroutines


| subroutine           | req. | bereq. | beresp. | obj. | resp. |
----------------------------------------------------------
| vcl_backend_fetch    |      |   R/W  |         |      |       |
| vcl_backend_response |      |   R/W  |   R/W   |      |       |
| vcl_backend_error    |      |   R/W  |   R/W   |      |       |
| vcl_recv             | R/W  |        |         |      |       |
| vcl_pipe             |      |   R/W  |         |      |       |
| vcl_pass             | R/W  |        |         |      |       |
| vcl_hash             | R/W  |        |         |      |       |
| vcl_purge            | R/W  |        |         |      |       |
| vcl_miss             | R/W  |        |         |      |       |
| vcl_hit              | R/W  |        |         | R    |       |
| vcl_deliver          | R/W  |        |         | R    | R/W   |
| vcl_synth            | R/W  |        |         |      | R/W   |
