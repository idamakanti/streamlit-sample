import streamlit as st
import json
import streamlit.components.v1 as components  # Import Streamlit
req =" {sample request here}"
res =" {turn response here}"
st.sidebar.title(" POC")

st.title("POC - API Catalog tool")
st.sidebar.selectbox("Select API Name ",("API Name1","API Name2"))
st.sidebar.selectbox("Select Version",("v1","v2"))
submit = st.sidebar.button('Submit', key='submit')

def loadpage():
	
	st.text_area('Input as Request JSON',req,height=400)
	run = st.button("Submit")
	st.text_area('Response',res,height=400)
	st.success("Success!")
		

def main():

	if submit:
		loadpage()

if __name__ == '__main__':
    main()
 

