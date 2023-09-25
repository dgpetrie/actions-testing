## vcon.filter_plugins.impl.whisper.Whisper

  **FilterPlugin** to generate transcriptions for a **Vcon**


**Methods**:

### \_\_init__
\_\_init__(self, init_options: vcon.filter_plugins.impl.whisper.WhisperInitOptions)

Parameters:
  init_options (WhisperInitOptions) - the initialization options for the Whisper trascription plugin


**init_options** - vcon.filter_plugins.impl.whisper.WhisperInitOptions

### filter(self, in_vcon: vcon.Vcon, options: vcon.filter_plugins.impl.whisper.WhisperOptions) -> vcon.Vcon


Transcribe recording dialogs in given Vcon using the Whisper implementation

Parameters:
  options (WhisperOptions)

  options.output_types List[str] - list of output types to generate.  Current set
  of value supported are:

   * "vendor" - add the Whisper specific JSON format transcript as an analysis object
   * "word_srt" - add a .srt file with timing on a word or small phrase basis as an analysis object
   * "word_ass" - add a .ass file with sentence and highlighted word timeing as an analysis object

  Not specifing "output_type" assumes all of the above will be output, each as a separate analysis object.

Returns:
  the modified Vcon with added analysis objects for the transcription.

### set_party_parameter

**set_party_parameter**(self, parameter_name: 'str', parameter_value: 'str', party_index: 'int' = -1) -> 'int'


Set the named parameter for the given party index.  If the index is not provided,
add a new party to the vCon Parties Object array.

Parameters:
  **parameter_name** (String) - name of the Party Object parameter to be set.
              Must beone of the following: ["tel", "stir", "mailto", "name", "validation", "gmlpos", "timezone"]
  **parameter_value** (String) - new value to set for the named parameter
  **party_index** (int) - index of party to set tel url on
              (-1 indicates a new party should be added)

Returns:
int: if success, positive int index of party in list



**options** - vcon.filter_plugins.impl.whisper.WhisperOptions

### \_\_del__(self)


Teardown/uninitialization method for the plugin

Parameters: None

