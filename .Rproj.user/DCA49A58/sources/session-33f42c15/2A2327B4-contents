#' Import Zip Files
#'
#' Take a URL for a zip folder and import into Posit Workbench
#' @param {zip_file} {A complete URL to the web-based zip folder that ends in .zip}
#' @param {name} {Defaults to imported_data, but a string for the name of the folder being created}
import_zip <- function(zip_file, name = "imported_data") {

  if(!endsWith(zip_file, ".zip")) {
    print("Not a zip folder. Please check the file location")
  }

  if(endsWith(zip_file, ".zip")) {
  download.file(zip_file, destfile = name) #download the zip
  unzip(name) #unpack the zip folder, into the directory
  unlink(name) #remove the weird "wk12" file that exists as it is no longer needed
  }

  }
