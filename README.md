| subroutine           | req. | bereq. | beresp. | obj. | resp. |
|----------------------|------|--------|---------|------|-------|
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
