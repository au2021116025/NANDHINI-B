import streamlit as st
import pickle



def get_Gene One():
    Gene One = st.text_input("gene one")
    return Gene One

def get_Gene Two():
    Gene Two= st.text_input("gene two")
    return Gene Two


def predict_species(GO,GT):
    loaded_model = pickle.load(open('knn_model.pkl','rb'))
    new_data = [[float(GO),float(GT)]]
    prediction = loaded_model.predict(new_data)
    st.write("Prediction with new data: ")
    st.write(prediction)
    



if __name__ == "__main__":
    st.title('Cancer prediction with KNN model')
    st.image('gene.png')    
    Gene One_value = get_Gene One()
    Gene Two_value = get_Gene Two()
    
    st.write("The parameters you entered are: ")
    st.write("Gene One ", Gene One_value)
    st.write("Gene Two ", Gene Two_value)
   

if st.button("Predict"):
    predict_species(Gene One_value,Gene Two_value)
