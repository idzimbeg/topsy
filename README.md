# Install

    Run `npm install topsysml` to install the dependencies.

# Usage

### First create a store

    import Store from 'topsysml'

### Than create action, mutation and initial state

    const actions = {
        saySomething(context, payload) {
        context.commit('setMessage', payload);
    }
    };

    const mutations = {
        setMessage(state, payload) {
        state.message = payload;

        return state;
        }

    };

    const initialState = {
        message: 'Hello, world'
    };

### Than instantiate the store

    const storeInstance = new Store({
        actions,
        mutations,
        initialState
    });
