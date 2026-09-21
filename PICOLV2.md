# PicoLV2 integration

Define `PICOLV2` when compiling the resampler sources for PicoLV2. This replaces
the resampler table's pthread mutex with a no-op implementation because the
firmware invokes each plugin instance from one core and does not provide
pthreads.

The DSP source and API are otherwise unchanged.
