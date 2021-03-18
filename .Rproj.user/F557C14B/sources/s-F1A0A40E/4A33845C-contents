

#' Title
#'
#' @param x
#' @param datasources
#'
#' @return This function simply returns the integer value 1
#' @export
#'
#' @examples
#'
ds.returnOne <- function(x=NULL, datasources=NULL){

  # look for DS connections
  if(is.null(datasources)){
    datasources <- datashield.connections_find()
  }

  # call the server side function that does the operation
  cally <- call("returnOneDS")
  result <- DSI::datashield.aggregate(datasources, cally)

  # names of the studies to be used in the output
  stdnames <- names(datasources)
  outputnames <- c()
  for (i in 1:length(datasources)){
    outputnames[i] <- paste0('Returning 1 for ', stdnames[i])
  }

  return(result)


}
